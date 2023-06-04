# Data-Modeling-with-Postgres
## Introduction
A new music streaming startup company called Sparkify is looking to analyze data about song data and user activity that they gave been collecting on their music streaming app. They are particulary looking to understand what songs the users are listening to regularly. Their data is currently in a directory of JSON logs on the user activity and songs in their app. They do not have an easy way to query their data currently.

## Project Description
They would like a data engineer to create a Postgres database with tables to give them an easy way to query their data. The goal of this project will be, building an ETL pipeline using python and data modeling with Postgres, defining fact and dimesion tables for a star schema geared towards a specific analylitical focus. THis will optimize queries allowing for easier analysis of thier song data and user activity. 



#### Schema for Song Play Analysis
The goal is to create a star schema for queries on song play analysis with a Fact Table and Dimensions table. 

**Fact Table:** 
songplays records log data associated withtsong plays, this table will have the following columns:
- songplay_id
- start_time
- user_id
- level
- song_id
- artist_id
- session_id
- location
- user_agent

**Dimesions Tables**
There will be the following dimesion tables to make up the star schema. 
- users table which includes: user_id, first_name, last_name, gender and level. 
- songs table which includes: song_id, title, artist_id, year, duration
- artists table which includes: artist_id, name, location, latitude, longitude
- time table which includes timestamps of the songplays broken down into the follwing columns: start_time, hour, day, week, month, year, weekday

## Project Files

There are six files used in this project: 

1. **test.ipynb** is used to test your code to make sure that the tables have been created and it will display the first few rows of each table for conformation. 
2. **create_tables.py** drops and creates tables, this is run to reset the tables created before re-running the ETL scripts. 
3. **etl.ipynb** is used to read and process a file from the song_data and log_data files. This file is used to load the data directly into the tables created. 
4. **etl.py** is also used to process files form song_data and log_data files and load them into your table. 
5. **sql_queries.py** holds all of the sql queries used and is imported and used in the create_tables.py, etl.py and etl.ipynm. 
6. **README.md** provides information and goals about this project.

## How to Run 
Once the create statments and DROP statements have been created in sql_queries to create each table: 
Run create_tables.py to create the database and tables. 
Run test.ipynb to confirm the creation of your tables with the correct columns.
After completing etl.ipynb and etl.py to develop ETL processes for each table.
Run etl.py to process for loading, extracting and inserting data into the tables and process the entire dataset.  
