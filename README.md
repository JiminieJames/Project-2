Crowdfunding ETL Mini Project

Team 13 James Brannan and John Haynes 

The series of code was created in part between the two team members, Xpert AI and tutor Justin Moore

Welcome to the Crowdfunding ETL Mini Project! In this project, you will work with a partner to build an ETL pipeline using Python, Pandas, and either Python dictionary methods or regular expressions to extract and transform data. Once transformed, you'll create CSV files, design an ERD and table schema, and finally, upload the data into a Postgres database.

Project Overview
This is a one-week project, so it's crucial to complete at least half of the project by the third day of class to stay on track. Although tasks will be divided between you and your partner, collaboration and communication are essential. Regular check-ins and mutual support will ensure the project's success.

Project Setup
Files
Download the starter code and files to help you get started: [Project 2 ETL files](link to files).

Repository Setup
Create Repository: One member of your group should create a new repository named Crowdfunding_ETL and add the other member as a collaborator. Do not add this project to an existing repository.
Clone Repository: Clone the new repository to your computer.
Rename Starter Code: Rename the ETL_Mini_Project_starter_code.ipynb file with the first name initial and last name of each group member (e.g., ETL_Mini_Project_NRomanoff_JSmith.ipynb). Add this Jupyter notebook file and the Resources folder containing crowdfunding.xlsx and contacts.xlsx to your repository.
Push and Pull Changes: Push the changes to GitHub. Have your partner pull the changes so both of you have the same notebook on your computers.
Work Distribution: You may work on different notebooks individually but combine all sections into the final ETL_Mini_Project notebook upon completion.
Instructions
The instructions are divided into the following sections:

Create the Category and Subcategory DataFrames
Create the Campaign DataFrame
Create the Contacts DataFrame
Create the Crowdfunding Database
1. Create the Category and Subcategory DataFrames
Category DataFrame: Extract and transform the data from crowdfunding.xlsx to create a category DataFrame with the following columns:

category_id: Entries sequentially from "cat1" to "catn"
category: Category titles
Subcategory DataFrame: Extract and transform the data from crowdfunding.xlsx to create a subcategory DataFrame with the following columns:

subcategory_id: Entries sequentially from "subcat1" to "subcatn"
subcategory: Subcategory titles
Export both DataFrames as category.csv and subcategory.csv, and save them to your GitHub repository.

2. Create the Campaign DataFrame
Extract and transform the data from crowdfunding.xlsx to create a campaign DataFrame with the following columns:

cf_id
contact_id
company_name
description (renamed from "blurb")
goal (float data type)
pledged (float data type)
outcome
backers_count
country
currency
launch_date (renamed from "launched_at" and converted to datetime format)
end_date (renamed from "deadline" and converted to datetime format)
category_id (matching the category_id in the category DataFrame)
subcategory_id (matching the subcategory_id in the subcategory DataFrame)
Export the campaign DataFrame as campaign.csv and save it to your GitHub repository.

3. Create the Contacts DataFrame
Choose one of the following options to extract and transform the data from contacts.xlsx:

Option 1: Python Dictionary Methods

Import contacts.xlsx into a DataFrame.
Iterate through the DataFrame, converting each row to a dictionary.
Extract values from keys using a list comprehension.
Create a new DataFrame with the extracted data.
Split the "name" column into "first_name" and "last_name".
Clean and export the DataFrame as contacts.csv.
Option 2: Regular Expressions

Import contacts.xlsx into a DataFrame.
Extract contact_id, name, and email columns using regular expressions.
Create a new DataFrame with the extracted data.
Convert contact_id to integer type.
Split the "name" column into "first_name" and "last_name".
Clean and export the DataFrame as contacts.csv.
4. Create the Crowdfunding Database
Inspect the four CSV files and sketch an ERD using QuickDBD.
Create a table schema for each CSV file, specifying data types, primary keys, foreign keys, and other constraints.
Save the database schema as a Postgres file named crowdfunding_db_schema.sql and save it to your GitHub repository.
Create a new Postgres database named crowdfunding_db.
Using the schema, create tables in the correct order to handle foreign keys.
Verify table creation by running a SELECT statement for each table.
Import each CSV file into its corresponding SQL table.
Verify that each table has the correct data by running a SELECT statement for each.
Hints
Use df[["new_column1","new_column2"]] = df["column"].str.split() to split column values.
Use NumPy arrays and list comprehensions to create unique IDs.
Refer to Pandas documentation for creating DataFrames, converting data types, and merging DataFrames.
Use the astype() method to convert columns to float.
See the Transform_Grocery_Orders_Solved.ipynb activity solution for converting UTC times to datetime format.
Support and Resources
Your instructional team will provide support during classes and office hours. Learning assistants and tutors are also available to help with topics as needed. Make sure to utilize these resources and collaborate with your partner effectively.