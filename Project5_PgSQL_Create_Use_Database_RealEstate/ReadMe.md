# Project5_PgSQL_Create_Use_Database_RealEstate

Here I create and use a 3NF-compliant database in pgSQL based on non-3NF compliant data.

In this project I use the software [DBeaver](https://dbeaver.io/download/) as a database driver.
You can find the slides I used to present my work [here](https://github.com/VivienPichon/Portfolio_Data_analyst/blob/060c86957a9c439b19cd8b906ea11299f639fa1e/Project5_PgSQL_Create_Use_Database_RealEstate/presentation_slides.pdf).

## Roleplay context

In this project, I work for a real estate company.
The CEO wants a tool to follow the evolution of the price of real estate based on open source real estate data.
This tool would be a relational database that we can query to get statistics based on the geographical area, demography and features of the properties sold.
I am tasked with creating a test version of this database with a limited amount of data:

- The real estate sales data of the first 6 month of 2020,
- The French Geographic Information table.
- The French Census results for 2020.

## Database design

The first task was to analyse the three table and create the structure of the database to make it 3NF compliant.
I created the [data dictionnary](https://github.com/VivienPichon/Portfolio_Data_analyst/blob/060c86957a9c439b19cd8b906ea11299f639fa1e/Project5_PgSQL_Create_Use_Database_RealEstate/data_dictionnary.pdf) available here to see more clearly.
In this document, the 3 first tables are the original tables that were given to me, and the 3 last tables are the 3NF-compliant tables.
The Real Estate table was split into 2 different tables: 
The sales table, which lists every single sale, and the property table, which gives all the characteristics of the property sold.
The Geographic Information table and Census results were grouped into one geographic area table.

After reshaping the data, I created the database using pgAdmin, and started querying using DBeaver.

## Database query

I was requested to make 13 different queries of various complexity to test the reliability of the database.
The code and results of the query can be checked in [the slides linked above](https://github.com/VivienPichon/Portfolio_Data_analyst/blob/060c86957a9c439b19cd8b906ea11299f639fa1e/Project5_PgSQL_Create_Use_Database_RealEstate/presentation_slides.pdf).

The database worked as intended.
