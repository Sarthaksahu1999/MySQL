This project demonstrates SQL filtering techniques in MySQL using a Sales Transactions dataset.
It includes practical queries to filter, sort, and analyze transaction data using SQL clauses such as WHERE, GROUP BY, HAVING, and ORDER BY.

Author: Sarthak Sahu

Project Overview

The goal of this project is to practice data filtering and aggregation in MySQL using a realistic sales dataset.

The queries cover:

Basic filtering using WHERE

Logical conditions using AND

Date filtering

Range filtering using BETWEEN

Handling missing values with IS NULL

Sorting results with ORDER BY

Aggregating data using GROUP BY

Filtering aggregated results using HAVING

These queries help in understanding how SQL can be used to analyze business transaction data efficiently.

Dataset Information

Dataset: Sales Transactions

Columns used in the dataset:

Column	Description
transaction_id	Unique ID for each transaction
transaction_date	Date when the transaction occurred
category	Product category (Electronics, Furniture, etc.)
amount	Transaction amount
payment_method	Method used for payment
region	Region where the transaction occurred

The dataset is stored in Excel format and can be imported into MySQL for analysis.

SQL Concepts Demonstrated

This project demonstrates the following SQL concepts:

WHERE clause filtering

Logical operators (AND)

Date-based filtering

Range filtering (BETWEEN)

Handling missing values (IS NULL)

Sorting with ORDER BY

Aggregation using GROUP BY

Filtering aggregated results using HAVING

Aggregate functions such as:

COUNT()

SUM()

AVG()

Example query:

SELECT *
FROM sales_transactions
WHERE category = 'Electronics'
AND amount > 500;

This query retrieves Electronics transactions with an amount greater than $500. 

Filtering In my_sql

Files in this Repository
File	Description
Sales Transactions.xlsx	Dataset used for analysis
Filtering In my_sql.docx	SQL queries written for MySQL practice
Filtering_in_SQL_DPP.pdf	Assignment document with queries and explanations

The PDF contains 10 SQL filtering queries along with explanations demonstrating different filtering techniques. 

Filtering_in_SQL_DPP

Learning Outcomes

By completing this project, you will learn how to:

Filter records from datasets using SQL

Analyze sales data using aggregation

Work with conditional filtering

Perform basic data analysis using MySQL queries

Technologies Used

MySQL

SQL

Microsoft Excel

GitHub
