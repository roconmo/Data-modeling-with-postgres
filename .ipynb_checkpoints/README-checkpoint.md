#### Sparkify project

The aim of this project is to create a Postgres database with tables designed to optimize queries on song play analysis. There are defined 4 dimension tables and 1 fact tables in a star schema. The **fact table** is songplays and the **dimension** tables are: songs, artists, users and time.

There are 3 files in the repository:

create_tables.py
In this jupyter notebook, there are functions to delete and create sparkify database.

sql_queries.py
In this jupyter it can be found queries to create, insert, delete tables and a query to select data. 

etl.py
This is the main jupyter notebook to access the log file, create postgress database and populate tables.
There are two main functions: 
-function process_song_file: given a cursor and a filepath, the functions inserts song and artists data in the database [L10](https://github.com/roconmo/Data-modeling-with-postgres/blob/cf253877c1f917600a4e1e9f2f1e9f6bd10a1dca/etl.py#L10)
-function process_log_file : given a cursor and a filepath, the functions inserts users, songplays and time data in the database [L29](https://github.com/roconmo/Data-modeling-with-postgres/blob/cf253877c1f917600a4e1e9f2f1e9f6bd10a1dca/etl.py#L29)
Other functions are:
- process_song_file: 

#### How to run the solution:
```
$ python create_tables.py 
```
To create Sparkify database, fact and dimesion tables
```
$ python etl.py
```
To populate the tables