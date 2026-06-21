# MYsql
Daily MySQL &amp; SQL practice repository covering basics to advanced queries, joins, aggregations, subqueries, window functions, LeetCode SQL problems, and real-world data analysis exercises. Focused on improving problem-solving and data analytics skills through consistent hands-on practice.
-- =========================================
-- DATA FLOW: EXCEL/CSV SHEET → MYSQL DATABASE
-- =========================================

CREATE DATABASE company_data;

USE company_data;

-- Create Table
CREATE TABLE employees (
    emp_id INT PRIMARY KEY,
    name VARCHAR(100),
    department VARCHAR(50),
    salary INT,
    joining_date DATE
);

-- Insert Data (Example from Sheet)
INSERT INTO employees
VALUES
(101, 'Prince', 'Data Analyst', 45000, '2026-01-10'),
(102, 'Rahul', 'HR', 35000, '2026-02-15'),
(103, 'Aman', 'Developer', 60000, '2026-03-01');

-- View Stored Data
SELECT * FROM employees;

-- Data Analysis Example
SELECT department, AVG(salary) AS average_salary
FROM employees
GROUP BY department;
