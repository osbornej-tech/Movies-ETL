# Movies-ETL
## Overview
In this repository, users will find 4 Juypter notebooks with each notebook building on the other. The notebooks are entitled:
* ETL_function_test.ipynb
* ETL_clean_wiki_movies.ipynb
* ETL_clean_kaggle_data.ipynb
* ETL_create_database.ipynb

In ETL_function_test, users will find the foundation code for establishing a extract transform and load function that uses list comprehension,  2 csv files and a json file. This file is the first file that allow users to complete a exploratory analysis of the data that would be used throughout this repository. 

ETL clean wiki movies uses three functions to  clean and a create movies dataframe. The functions in this notebook include: clean movie, change column name, parse dollar and extract transform and load function. The clean movies function removie movies with alternative title. The change column name formats the column names with more appropriate titles such as running time, release date rather than length and orginal release, respectively. The extract transform and load function remove all tv shows,take the clean movies and add them to a dataframe.This function utilize regular expression to parse box office values, find IMDb Ids, release date, running time and budget. Additionally, this function request the input of three data files that are formatted and analyzed for use in the remaining notebooks. 

ETL Kaggle notebook utilizes the function of the clean wiki notebook amd include a few additional lines of code that is specific to the kaggle data. Cleaning the kaggle data include modifying the column type for the budget, id, popularity, release date and timestamp columns. Furthermore, this notbook merges the wiki_movie dataframe and the kaggle data on the ID field. Then, that dataset is merged with the ratings data set on the Id field using a left join. Some columns are renamed and some columns (title, release date, language and production company) are dropped 

ETL create_database merges the data from the ratings, wiki and kaggle movie information to create a database with 2 tables one containing movies and the other movie ratings. The data is added to a local SQL server that an be utilized for further analysis. 

The data yield a movie table that contains: 
<img src ='https://github.com/osbornej-tech/Movies-ETL/blob/main/movies_query.png'> rows,

and a ratings table that contains:
<img src ='https://github.com/osbornej-tech/Movies-ETL/blob/main/ratings_query.png'> rows.


Tools:
PostgreSql -pdAdmin server
Juypter - Anaconda
