📌 Data Retrieval in SQL (MySQL)
👨‍🎓 Student Details

Name: Sarthak Sahu

Topic: DISTINCT, LIMIT, ORDER BY & Query Optimization

Database Used: orders_db

📖 Assignment Overview

This assignment focuses on practical SQL query writing and optimization techniques in MySQL, covering:

Using DISTINCT to remove duplicate values

Applying LIMIT for controlled output

Sorting results with ORDER BY

Improving performance through indexing

Understanding execution plans with EXPLAIN

Writing real-world optimized queries

📄 Assignment Document Included Here:


Data_Retrieval_In_SQL

🗂 Dataset Used

The queries are based on an e-commerce orders table:

order_id	customer_id	product_name	order_date
101	200	Laptop	2025-01-15
102	201	Phone	2025-01-16
...	...	...	...
✅ Concepts Covered
1️⃣ Practical Use of DISTINCT
🔹 Unique Products Ordered
SELECT DISTINCT product_name
FROM orders;

🔹 Count Unique Products per Customer
SELECT customer_id,
       COUNT(DISTINCT product_name) AS unique_products
FROM orders
GROUP BY customer_id;

2️⃣ Combining DISTINCT + ORDER BY + LIMIT
🔹 Top Recent Unique Products
SELECT DISTINCT product_name
FROM orders
ORDER BY order_date DESC
LIMIT 3;

🔹 Customer-Specific Recent Orders
SELECT DISTINCT product_name
FROM orders
WHERE customer_id = 200
ORDER BY order_date DESC
LIMIT 3;

3️⃣ Query Optimization with Indexing
📌 Recommended Indexes
CREATE INDEX idx_order_date ON orders(order_date);
CREATE INDEX idx_product_name ON orders(product_name);


Indexes help reduce:

Full table scans

Sorting overhead

Duplicate elimination cost

4️⃣ Execution Plan Analysis
🔍 Using EXPLAIN
EXPLAIN
SELECT DISTINCT product_name
FROM orders
WHERE order_date >= CURDATE() - INTERVAL 30 DAY
ORDER BY order_date DESC
LIMIT 10;


This helps identify:

Missing indexes

Temporary table usage

Slow sorting operations

5️⃣ Real-World Complex Query
🔹 Customer Who Ordered Each Product Most Recently
SELECT o.product_name,
       o.customer_id,
       o.order_date
FROM orders o
JOIN (
    SELECT product_name,
           MAX(order_date) AS last_order
    FROM orders
    GROUP BY product_name
) latest
ON o.product_name = latest.product_name
AND o.order_date = latest.last_order;

📂 Repository Files
File Name	Description
Data_Retrieval_In_SQL.pdf	Full assignment solution document
mysql_distinct_limit_orderby_optimization.sql	SQL script with all queries

SQL Script Reference:


mysql_distinct_limit_orderby_op…

🚀 How to Run This Project

Create database:

CREATE DATABASE orders_db;
USE orders_db;


Create the orders table and insert sample data

Run queries from:

mysql_distinct_limit_orderby_optimization.sql

⭐ Key Learning Outcomes

✔ Efficient use of DISTINCT
✔ Sorting and limiting results
✔ Performance tuning with indexes
✔ Understanding query execution
✔ Writing scalable real-world SQL queries

📌 Author

Sarthak Sahu
