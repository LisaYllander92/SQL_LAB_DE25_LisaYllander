# Introduction
This repo is for the LAB in the SQL course where we'll be working with the sakila database and analysing data using duckdb and pandas in jupyter notebook and later on Evidence dashboard.

# Tasks 

### Task 0 - data ingestion
- Creating the repo 
- Install: 
    - uv init (virtuell inviorment)
    - duckdb (querys)
    - pandas (for analysing data)
    - ipykernel (for jupyter notebook)
    - matplotlib (for drawing graphs)

### Task 1 - EDA in python
- Using sql queries in jupyter notebook to show the result directly. 
- Combining duckdb and pandas to do the EDA.
- To perform the EDA I've used aggregation function, some regular expressions, JOINs to join nessesary data from diffrent tables, CAST function to convert and timezone functions. 

### Task 2 - graphs
- Using matplotlib to visualize some resluts.

### Task 3 - BI report
- Using Evidence dashboard to create my own dashboard and showing some of my findings from previous tasks. 

- Setup - data load tool (dlt):
    - uv add "dlt[sql_database]" "dlt[parquet]"
    - Create and load sakila sqlite to duckdb:
        - import dlt
        - from dlt.sources.sql_database import sql_database
    - Create path: 
        - from pathlib import Path
    - See 'load_sakila_sqlite_duckdb.py'

- Setup evidence dashboard:
    - install nodejs version 22
    - install extension - 'Evidence'
    - create new evidence project in 'dashboard' folder
- Install and run: 
- NOTE: make sure to stand in 'dashboard' folder
    - npm install (installing all dependencies needed)
    - npm run sources (to setup data sources difined under sources folder)
    - npm run dev (to start the evidence server)



## Sources
- Installations and loading sakila: 
    - https://www.youtube.com/watch?v=GiAZXBaBbDk 

    - https://www.youtube.com/watch?v=nFbKOa-_YKw

- Pattern matching: 
    - https://duckdb.org/docs/stable/sql/functions/pattern_matching
    - https://www.geeksforgeeks.org/postgresql/postgresql-regexp_matches-function/ 

- Aggregation functions:
    - https://www.youtube.com/watch?v=4U7tAck5zUA 

- Converting:
    - https://www.w3schools.com/sql/func_sqlserver_cast.asp 

- Timestamp:
    - https://duckdb.org/docs/stable/sql/functions/timestamptz

- Subquery:
    - https://www.youtube.com/watch?v=aZQtKjWfaDw 

- Joins:
    - https://www.w3schools.com/sql/sql_join.asp

- Plotting:
    - https://www.youtube.com/watch?v=nFbKOa-_YKw

- Working with dashboard:
    - https://www.youtube.com/watch?v=8jMIRtGwReY
    - index.md (Evidence dashboard)
    - Kokchuns brain (helpt me with linechart)

## Sakila database
![Table overview](Sakila_overview.png)