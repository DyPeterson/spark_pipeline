## DSA Spark code review

###  Contributors:

- [Dylan Peterson](https://github.com/DyPeterson)

###  Description

A [Data Stack Academy](https://www.datastack.academy/) code review project that takes a [`coffee.csv`](https://www.kaggle.com/datasets/psycon/daily-coffee-price). With that CSV it creates a start to finish pipeline. All using Apache Spark

###  Technologies Used:

- [Python](https://www.python.org/)

- [Apache Spark](https://spark.apache.org/)

- [Jupyter Notebooks](https://jupyter.org/)

- [Pandas](https://pandas.pydata.org/)

- [Matplotlib](https://matplotlib.org/)

####  Programs used:

- [Visual Code Studio](https://code.visualstudio.com/)

- [Windows Terminal](https://apps.microsoft.com/store/detail/windows-terminal/9N0DX20HK701?hl=en-us&gl=US) ( Running: [WSL2](https://docs.microsoft.com/en-us/windows/wsl/install) ([ubuntu 20.04](https://releases.ubuntu.com/20.04/)))


###  Setup & Installation:


1. Through the terminal like [GitBash](https://git-scm.com/downloads)

	2. Open the terminal and navigate to where you would like the new project to be using `cd` commands. Its also recommended that you make a new directory using `mkdir *directory-name*`.

	3. Clone the repository using the command `git clone https://github.com/DyPeterson/spark_pipeline.git`

	4. After cloning the directory it will appear in the directory that your terminal is set to. So make sure you are in the directory that you want this project copied to.

	5. Once this project is cloned you can navigate to that folder within your terminal and create a virtual environment `python3.7 -m venv *any-name*`. Now activate the venv with `source *any-name*/bin/activate`

	6. Install requirements in venv `pip install -r requirements.txt`
	
    7. Download the [kaggle dataset](https://www.kaggle.com/datasets/psycon/daily-coffee-price) and place inside the repository's `data` folder 

	8. `code .` to open in default coding software.

2. Through GitHub.com

	9. Go to the project's directory page **[HERE](https://github.com/DyPeterson/spark_pipeline)**

	10. Click the green `code` button to open the drop-down menu.

	11. At the bottom of the menu will have *Download Zip*. Go ahead and click it to download the project.

	12. Once downloaded find the `.zip` file and right-click it to bring up the menu. Within that menu click `Extract Here` to extract it in the current folder or click `Extract Files...`to select which folder you would like the project in.
	
    13. Download the [kaggle dataset](https://www.kaggle.com/datasets/psycon/daily-coffee-price) and place inside the repository's `data` folder 

	14. Once the project has been extracted, locate the folder in a terminal and open it with `code .` .

3. Once opened in your IDE of choice, run the jupyter cells in order.

###  Useful Links

####  Link to project on GitHub:

[GitHub Repository](https://github.com/DyPeterson/spark_pipeline)

###  Details
This project uses Apache Spark to load a CSV into a DataFrame and profile, clean, and query the data. The process of the pipeline is as follows:
1. Loads CSV into a spark dataframe setting the schema as well

2. Add multiple columns:

    1. `daily_price_change` - Difference between `Open` and `Close` 
    prices

    2. `daily_fluctuation` - Difference between `High` and `Low`

    3. `vol_over_100` - Boolean(true/false) column indicating if the daily volume is over 100

    4. `daily_price_swing` - Absolute value of `daily_price_change`

    5. `net_sales`- Calculates the average of `high`, `low`, `open`, & `close` and multiplies it by the `volume` giving us the net sales

3. Calculates stats:

   1. Average of `daily_price_swing`

   2. Count of days that did not pass 100 Volume

   3. Average of `Open` values

   4. Highest value of `High`

4. Saves the new data as a parquet file.

Contact me with any questions or suggestions [Here](dylan.peterson17@gmail.com)

###  Known Bugs

No known bugs at this time.

###  Copyright 2022

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.