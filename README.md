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


## Transformation 
* For each of the datasets
  * Identified data columns relevant tot he proposed inquiry
  * Created or used a year column from an existing data column
  * Formatted the year column to the same data type in each DataFrame
  * Created new Dataframes with the columns relevant to the proposed inquiry
The above-described process for one of the DataFrames
