# Day 1 SQL Practice

-- Get all columns from employees
SELECT * FROM employees;

-- Get specific columns
SELECT name, salary FROM employees;

-- Filter with WHERE
SELECT * FROM employees WHERE salary > 50000;

-- Order by salary highest to lowest
SELECT * FROM employees ORDER BY salary DESC;

-- Exclude HR department
SELECT * FROM employees WHERE NOT department = 'HR';
