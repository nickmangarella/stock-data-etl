# stock-data-etl

## Project Team:
Jordan Gilmartin, Lynell Robinson, Min Xie, Nick Mangarella, Sushama Kunnath

## Introduction
For this ETL project, we used Kaggle as our public source data platform. The datasets are based on the New York Stock Exchange S&P 500 company’s historical prices with fundamental data ranging over various years from 2010 to 2016. The datasets include are:

*	Fundamental Data - https://www.kaggle.com/dgawlik/nyse?select=fundamentals.csv 
*	Security Data - https://www.kaggle.com/dgawlik/nyse?select=securities.csv 
*	Prices Data - https://www.kaggle.com/dgawlik/nyse?select=prices.csv 

## Extraction
* Identified the dataset file types
  * All of our datasets originate from csvs
* Extracted the data from each of the CSV files and loaded the data into separate DataFrames
One of the converted CSV files to a DataFrame
[!alt text](https://github.com/nickmangarella/stock-data-etl/blob/master/images/Figure1.png)

## Transformation 
* For each of the datasets
  * Identified data columns relevant tot he proposed inquiry
  * Created or used a year column from an existing data column
  * Formatted the year column to the same data type in each DataFrame
  * Created new Dataframes with the columns relevant to the proposed inquiry
Figure 2: The above-described process for one of the DataFrames
[!alt text](https://github.com/nickmangarella/stock-data-etl/blob/master/images/Figure2-1.png)
[!alt text](https://github.com/nickmangarella/stock-data-etl/blob/master/images/Figure2-2.png)
[!alt text](https://github.com/nickmangarella/stock-data-etl/blob/master/images/Figure2-3.png)
* Merged the three datasets on the Ticker Symbol and Year
Figure 3: One of the emrged DataFrames
[!alt text](https://github.com/nickmangarella/stock-data-etl/blob/master/images/Figure3.png)

* Cleaned the DataFrame
  * Dropped the null values within the new dataset 
  * Dropped the duplicate ticker symbols
Figure 4: Cleaning of the DataFrame
![alt text](https://github.com/nickmangarella/stock-data-etl/blob/master/images/Figure4.png)

* Formatted the DataFrane
  * Formatted the year column
  * To make the exponential column data more readable
   * Divided by either a billion or million
   * Formatted the decimal places
   * Renamed the column to represent the exponent (B or M)
  * Replaced all spaces within the coumn names to underscores for simpler table name conversion
Figure 5: Formatting of the DataFrame and the Final DataFrame result
![alt text](https://github.com/nickmangarella/stock-data-etl/blob/master/images/Figure5-1.png)
![alt text](https://github.com/nickmangarella/stock-data-etl/blob/master/images/Figure5-2.png)
![alt text](https://github.com/nickmangarella/stock-data-etl/blob/master/images/Figure5-3.png)
![alt text](https://github.com/nickmangarella/stock-data-etl/blob/master/images/Figure5-4.png)
![alt text](https://github.com/nickmangarella/stock-data-etl/blob/master/images/Figure5-5.png)

## Load
* Connected to the PostgreSQL database
* Used pandas to load the merged, converted DataFrame into the database
Figure 6: The load process into a PostgreSQL Database
![alt text](https://github.com/nickmangarella/stock-data-etl/blob/master/images/Figure6.png)
