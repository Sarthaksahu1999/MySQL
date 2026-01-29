📘 Introduction to SQL and Databases (MySQL Assignment)

Prepared By: Sarthak Sahu
Database System: MySQL
Topic: SQL Basics, Filtering, Data Modification & Constraints

📌 Overview

This assignment provides a foundational understanding of SQL (Structured Query Language) and relational databases using MySQL.
It includes database creation, table design, inserting records, querying data, applying conditions, modifying records, and implementing constraints for data integrity.

🎯 Objectives Covered

The assignment focuses on the following key SQL concepts:

Creating and using databases

Designing tables with primary keys

Inserting employee records

Retrieving and filtering data using WHERE

Modifying records using INSERT, UPDATE, and DELETE

Applying constraints such as NOT NULL, UNIQUE, and CHECK

Understanding schema evolution through enhanced tables

🗂️ Assignment Tasks
✅ 1. Database & Table Creation

Created a database named company_db

Designed an employees table with the following attributes:

Column Name	Description
id	Primary Key
first_name	Employee First Name
last_name	Employee Last Name
department	Department Name
salary	Monthly Salary
✅ 2. Inserting Employee Records

Inserted initial employee data into the employees table.

Example:

INSERT INTO employees VALUES
(1,'John','Doe','Sales',45000),
(2,'Jane','Smith','HR',52000);

✅ 3. Retrieving Records

Fetched all employee records using:

SELECT * FROM employees;

✅ 4. Filtering Data Using WHERE Clause

Performed filtering based on conditions:

Employees from Sales department

Employees earning more than 50000

Sales employees earning above 50000

Example:

SELECT * FROM employees
WHERE department='Sales' AND salary > 50000;

✅ 5. Modifying Data (DML Operations)

Used SQL Data Manipulation Commands:

INSERT additional employees

UPDATE salary of employee with ID = 2

DELETE employee with ID = 1

Example:

UPDATE employees SET salary=60000 WHERE id=2;
DELETE FROM employees WHERE id=1;

✅ 6. Using Constraints for Data Integrity

Created an enhanced table employees_v2 with constraints:

PRIMARY KEY

NOT NULL

UNIQUE

CHECK

Example:

CREATE TABLE employees_v2 (
    id INT PRIMARY KEY,
    name VARCHAR(50) NOT NULL,
    email VARCHAR(100) UNIQUE,
    salary INT CHECK (salary > 0)
);


Tested duplicate email insertion to verify UNIQUE constraint.

📊 Expected Output

Final employee table contains updated records after modification operations.

🧩 ER Diagram

The ER diagram (included on Page 3) represents the structure of:

employees table

Schema evolution into employees_v2 with constraints

Entities include:

Employee ID (Primary Key)

Names

Department

Salary

Email with unique constraint

📌 Key Learning Outcomes

By completing this assignment, you gain hands-on experience in:

SQL query writing

Database design principles

Record filtering and modification

Enforcing constraints for data consistency

Understanding schema evolution

🛠️ Tools Used

MySQL Workbench / MySQL CLI

SQL Commands (DDL + DML)

📁 Files Included

MYSQL_Introduction_To_Database.pdf

Introduction to SQL and Databases.docx

SQL Scripts (Queries Included)

✨ Author
SARTHAK SAHU

Sarthak Sahu
Aspiring Data Analyst | SQL & Database Learner
