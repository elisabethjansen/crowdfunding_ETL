# crowdfunding_ETL

This project was completed by An L. and Elisabeth J. to practice skills in extracting, transforming, and loading data. 

Data for this project was provided by Edx. Code used to extract and transform all tables can be found in the ETL_mini_project jupyter notebook file. 

The created DataFrames were exported to the Resources folder. 

Table schema and verification code can be found within the resources folder as schema.sql

## Project Documentation
Database Type: Relational (SQL)

Data Cleaning and Processing: Jupyter Notebook

Packages Used: pandas, numpy, datetime

Data Loading: pgAdmin

## Project Outline 
Create the Category and Subcategory DataFrames

1.Category DataFrame Creation

-Extract the data from the crowdfunding.xlsx file.
-Transform the data to create a DataFrame named category with the following columns:
category_id: This column should contain sequential entries from "cat1" to "catn", where n is the number of unique categories.
category: This column should contain only the category titles.
-Export the category DataFrame as category.csv.
-Save the category.csv file to your GitHub repository.

2.Subcategory DataFrame Creation

-Extract the data from the crowdfunding.xlsx file.
-Transform the data to create a DataFrame named subcategory with the following columns:
subcategory_id: This column should contain sequential entries from "subcat1" to "subcatn", where n is the number of unique subcategories.
subcategory: This column should contain only the subcategory titles.
-Export the subcategory DataFrame as subcategory.csv.
-Save the subcategory.csv file to your GitHub repository.

Create Campaign DataFrame 

1.Extract the data from the crowdfunding.xlsx file.
Transform the data to create a DataFrame named campaign with the following columns:
cf_id
contact_id
company_name
description (renamed from blurb)
goal (converted to the float data type)
pledged (converted to the float data type)
outcome
backers_count
country
currency
launch_date (renamed from launched_at and converted to datetime format with UTC times)
end_date (renamed from deadline and converted to datetime format with UTC times)
category_id (with unique identification numbers matching those in the category_id column of the category DataFrame)
subcategory_id (with unique identification numbers matching those in the subcategory_id column of the subcategory DataFrame)
Export Data

2.Export the campaign DataFrame as campaign.csv.
Save the campaign.csv file to your GitHub repository.

Create the Cotacts DataFrame 

1. Choose one of the two options for extracting and transforming data from the contacts.xlsx data:
   Option 1: Use regular expressions .
   Option 2: Use Python dictionary methods.
2. Option 1 is the following steps
   - Import the contacts.xlsx file into a DataFrame.
   - Iterate through the DataFrame, converting each row into a dictionary.
   - For each dictionary:
     - Extract the values using a Python list comprehension.
     - Add the values for each row to a new list.
   - Create a new DataFrame containing the extracted data.
   - Split each value in the name column into first_name and last_name columns.
   - Clean and export the DataFrame as contacts.csv.
   - Save the contacts.csv file to your GitHub repository.

3. Option 2 is the following steps
   - Import the contacts.xlsx file into a DataFrame.
   - Extract the "contact_id", "name", and "email" columns by using regular expressions.
   - Create a new DataFrame with the extracted data.
   - Convert the "contact_id" column to the integer type.
   - Split each "name" column value into a first and a last name, and place each in a new column.
   - Clean and then export the DataFrame as contacts.csv and save it to your GitHub repository.

  Create the Crowdfunding Database
  - Review the contents of the four CSV files.
  - Sketch an Entity-Relationship Diagram (ERD) for the tables using QuickDBD.
  - Use the information from the ERD to create a table schema for each CSV file.
  - Save the database schema as a Postgres file named crowdfunding_db_schema.sql.
  - Save the crowdfunding_db_schema.sql file to your GitHub repository.
  - Create a new Postgres database named crowdfunding_db.
  - Using the database schema, create the tables in the correct order to handle the foreign keys.
  - Verify the table creation by running a SELECT statement for each table.
  - Import each CSV file into its corresponding SQL table.
  - Verify that each table has the correct data by running a SELECT statement for each.


     









## Resources

Code guided by provided starter code, class activities, and aided in debuggin by the Xpert Learning Assistant. 
