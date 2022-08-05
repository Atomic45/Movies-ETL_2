# Movies-ETL_2

## Brief Summary

Amazing Prime would like an automated pipeline that takes in new data, performs the transformation, and loads the data into an existing tables. This process requires writing ETL functions to read three data files containing movie data. The following data files are as described: 

1. Kaggle metadata
2. MovieLens ratings (csv file as Pandas Dataframe)
3. Wikipedia movie data as json data file

Next, the process required to extract and transform the Wikipedia data to be able to merge with the Kaggle metadata. A try-except block was added to catch errors while extracting the IMDB IDs, which included dropping duplicates. The following columns were cleaned:

* Box office column
* Budget column
* Release date column
* Running time column

Third, several steps took place during this part of the process:

* The Kaggle metadata was cleaned.
* The Wikipedia and Kaggle dataframes were merged. 
     * Unneccessary columns were dropped. 
     * specific columns were kept. 
     * the movies_df dataframe columns were renamed. 
* The MovieLens ratings data was extracted and transformed. 

Finally, the Movie database was created using PostgreSQL. Two tables were created to view in the SQL query. 
