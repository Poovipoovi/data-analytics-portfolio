# Day 2 SQL Progress

## Topics Covered
- SQL Insert Into
- SQL Null Values
- SQL Update
- SQL Delete
- SQL Select Top
- SQL Aggregate Functions
- SQL Min and Max
- SQL Count
- SQL Sum
- SQL Avg

## Practice Queries

-- Count all employees
SELECT COUNT(*) FROM employees;

-- Get minimum and maximum salary
SELECT MIN(salary) AS min_salary, MAX(salary) AS max_salary FROM employees;

-- Get average salary
SELECT AVG(salary) AS avg_salary FROM employees;

-- Get sum of all salaries
SELECT SUM(salary) AS total_salaries FROM employees;

-- Count employees per department
SELECT department, COUNT(*) AS num_employees 
FROM employees 
GROUP BY department;

-- Get top 5 highest paid employees
SELECT * FROM employees 
ORDER BY salary DESC 
LIMIT 5;

-- Filter out null values
SELECT * FROM employees 
WHERE department IS NOT NULL;
