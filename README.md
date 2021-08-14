# Movies-ETL
An analysis of Wikipedia and Kaggle movie data.

## Purpose

The purpose of this challenge was to use Pandas dataframes with Python to extract, transform, and load dataframes into SQL databases. Dataframes were _extracted_ from csv files, _transformed_ by using functions to clean and merge the data, and _loaded_ through connection strings to SQL. Additionally, regular expressions (regex) and lambda functions were used to search and create consistent formatting in columns within the dataframes.

## Results

**Deliverable 1: Write an ETL Function to Read Three Data Files**

The wiki_movies_df, kaggle_metadata, and ratings dataframes were created by using a function (extract_transform_load) to read the raw csv and json files and convert the data into a DataFrame. This deliverable was completed to practice the "extract" portion of the ETL process and begin to "transform" the data.

<img width="836" alt="Screen Shot 2021-08-14 at 1 40 00 PM" src="https://user-images.githubusercontent.com/85946042/129460424-88bc96d2-cbe9-4475-bce6-d5dc269a4cfd.png">
<img width="837" alt="Screen Shot 2021-08-14 at 1 40 09 PM" src="https://user-images.githubusercontent.com/85946042/129460426-d2b686ef-9f90-49d2-bdca-d9023481795c.png">
<img width="263" alt="Screen Shot 2021-08-14 at 1 40 15 PM" src="https://user-images.githubusercontent.com/85946042/129460429-65edd9df-4ccf-4535-8b7f-02892f74ba57.png">


**Deliverable 2: Extract and Transform the Wikipedia Data**

The data in wiki_movies_df was cleaned by filtering out TV shows, removing columns that had null values, and streamlining the data format in columns to be consistent. The box office, budget, release date, and running time columns were cleaned in this process. The clean Pandas DataFrame is displayed and the clean column names are printed below.

<img width="842" alt="Screen Shot 2021-08-14 at 2 43 15 PM" src="https://user-images.githubusercontent.com/85946042/129460442-e8238137-557f-4656-82d2-37d0f9735988.png">
<img width="486" alt="Screen Shot 2021-08-14 at 2 43 24 PM" src="https://user-images.githubusercontent.com/85946042/129460446-6a656437-95d3-440b-a761-4c5dbc3ffc54.png">


**Deliverable 3: Extract and Transform the Kaggle data**

First, the kaggle metadata was cleaned to remove null values, inconsistent formatting and redundancies. Next, the wiki_movies_df and the kaggle_metadata dataframes were merged into a single dataframe, movies_df. The single merged dataframe was cleaned to remove or fill in empty data. Columns were dropped to remove redundant data. Next, the ratings data was merged into the movies_df to create movies_with_ratings_df. The movies_with_ratings_df, therefore, is the merged table from all three raw datasets. 

<img width="526" alt="Screen Shot 2021-08-14 at 4 29 23 PM" src="https://user-images.githubusercontent.com/85946042/129460466-07d4f3ab-f8c2-4295-8f8a-119e29891f86.png">
<img width="528" alt="Screen Shot 2021-08-14 at 4 29 08 PM" src="https://user-images.githubusercontent.com/85946042/129460474-9ad5acdf-a51f-4290-b1c3-682a38259a7e.png">
<img width="523" alt="Screen Shot 2021-08-14 at 4 29 52 PM" src="https://user-images.githubusercontent.com/85946042/129460481-b3d27e22-72fa-41f0-a5e9-cd3d1cf85e56.png">

**Deliverable 4: Create the Movie Database**

In the final step of the ETL process, the data was loaded into SQL. All 6,052 rows from the movies query were successfully loaded into the PostgreSQL "movies" table. All 26,024,289 rows from the ratings query were also successfully loaded into the PostgreSQL "ratings" table. The screenshots of these count queries and data from the first ten rows are included below to confirm that both tables were loaded into the movies_data database accurately.

<img width="642" alt="movies_query" src="https://user-images.githubusercontent.com/85946042/129460274-318d903a-effb-4e3b-a1c1-eff732cb508e.png">


<img width="1114" alt="Screen Shot 2021-08-14 at 4 49 43 PM" src="https://user-images.githubusercontent.com/85946042/129460958-e91fb6bc-5ffd-49e6-9460-f33c632403be.png">

<img width="617" alt="ratings_query" src="https://user-images.githubusercontent.com/85946042/129460278-d495f337-892f-4bcc-95e5-d126cb682849.png">

<img width="722" alt="Screen Shot 2021-08-14 at 4 50 07 PM" src="https://user-images.githubusercontent.com/85946042/129460960-e1ad5857-67d8-47ae-82f9-ae35ee0065fa.png">

## Summary
The ETL (extract, transform, load) process was successfully used to import cleaned data into PostgreSQL pgAdmin4 by using PythonData with Pandas in Jupyter Notebook. New concepts, such as regex and lambda functions, were utilized to extract and transform the data prior to loading. 
