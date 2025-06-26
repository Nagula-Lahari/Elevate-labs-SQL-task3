 Writing Basic SELECT Queries
This repository contains  The objective of this task is to demonstrate the ability to extract data from one or more tables using various SELECT query clauses.

Table of Contents
Project Objective

Tools Used

Deliverables

SQL Script Overview

Setup and Execution

Interview Questions & Answers

Project Objective
The main objective of this task is to gain a clear understanding of how to retrieve data from a relational database. This includes:

Selecting all columns (SELECT *) or specific columns.

Filtering rows using WHERE, AND, OR, LIKE, and BETWEEN clauses.

Sorting results using ORDER BY (ascending and descending).

Limiting the number of rows returned using LIMIT.

Tools Used
Database Management System: MySQL (or SQLite, PostgreSQL, etc.)

SQL Client: MySQL Workbench / DB Browser for SQLite (or any preferred SQL client)

Deliverables
task3_select_queries.sql: An SQL script file containing all the CREATE TABLE, INSERT, and SELECT query examples.

README.md: This file, explaining the project and answering interview questions.

(Optional) Screenshots folder: A folder (e.g., screenshots/) containing images of the query execution and results for visual confirmation.

SQL Script Overview
The task3_select_queries.sql file contains the following sections:

Table Creation: CREATE TABLE statements for two sample tables: Employees and Products, with predefined schemas.

Data Insertion: INSERT INTO statements to populate the Employees and Products tables with sample data. This data is used for demonstrating the SELECT queries.

SQL Query Examples: A series of SELECT statements demonstrating various clauses as required by the task:

SELECT * and selecting specific columns.

WHERE clause with AND, OR for filtering.

LIKE operator for pattern matching.

BETWEEN operator for range filtering.

ORDER BY for sorting (ascending and descending, single and multiple columns).

LIMIT for restricting the number of returned rows (including OFFSET).

Setup and Execution
To run the SQL script and observe the results:

Open your SQL Client: Launch DB Browser for SQLite, MySQL Workbench, or your preferred SQL client.

Connect to a Database Server: Establish a connection to your MySQL server (or open a new SQLite database).

Create a Database (Optional, for MySQL/PostgreSQL):

CREATE DATABASE Task3;
USE Task3;

(If using SQLite, you can simply open/create a .db file.)

Execute the Script: Open the task3_select_queries.sql file in your SQL client and execute the entire script. It will create the tables, insert the sample data, and then run each SELECT query, displaying its results.

Interview Questions & Answers
Key Concepts: Filtering, Projection
What does SELECT * do?
SELECT * is a SQL statement used to retrieve all columns from the specified table(s) or view(s). The asterisk (*) acts as a wildcard, representing every column in the table in the order they were defined.

How do you filter rows?
Rows in a SQL query are filtered using the WHERE clause. The WHERE clause specifies a condition or conditions that must be true for a row to be included in the result set. Multiple conditions can be combined using logical operators like AND, OR, and NOT.

What is LIKE '%value%'?
LIKE is a logical operator used in a WHERE clause to search for a specified pattern in a column. The % (percent sign) wildcard represents zero, one, or multiple characters. LIKE '%value%' finds rows where the column contains "value" anywhere within the string.

What is BETWEEN used for?
The BETWEEN operator is used in a WHERE clause to filter a range of values. It is inclusive, meaning it includes both the start and end values in the range specified (value1 and value2). It works with numbers, text, and dates.

How do you limit output rows?
You limit the number of output rows using the LIMIT clause. This clause is typically placed at the end of a SELECT statement and is very useful for pagination or retrieving only a subset of data. For example, LIMIT 10 returns the first 10 rows. LIMIT X OFFSET Y skips Y rows and then returns X rows.

Difference between = and IN?

= (Equals operator): Used to check for exact equality with a single value.

Example: WHERE Department = 'IT'

IN operator: Used to check if a value matches any value in a specified list of values. It's a shorthand for multiple OR conditions.

Example: WHERE Department IN ('HR', 'Sales') (equivalent to WHERE Department = 'HR' OR Department = 'Sales')

How to sort in descending order?
To sort results in descending order, you use the ORDER BY clause followed by the column name and the keyword DESC.

Example: ORDER BY Salary DESC

What is aliasing?
Aliasing in SQL involves giving a temporary, alternative name (an alias) to a table or a column within a query. This alias exists only for the duration of that specific query execution, improving readability.

Column Alias: SELECT FirstName AS FName FROM Employees;

Table Alias: SELECT E.FirstName FROM Employees AS E;

Explain DISTINCT.
The DISTINCT keyword is used in a SELECT statement to eliminate duplicate rows from the result set. When DISTINCT is applied, only unique combinations of the selected columns will be returned.

Example: SELECT DISTINCT Department FROM Employees; will return each unique department name only once.

What is the default sort order?
The default sort order in SQL (when using ORDER BY without explicitly specifying ASC or DESC) is ascending order (ASC). This means numbers are sorted smallest to largest, text alphabetically (A to Z), and dates from oldest to newest.
