# Day 4 SQL - JOINs Mastery

## Topics Covered
- SQL Joins (concept)
- SQL Inner Join
- SQL Left Join
- SQL Right Join
- SQL Full Join

## Practice Queries

-- INNER JOIN: Get employees with their department names
SELECT employees.name, employees.salary, departments.dept_name
FROM employees
INNER JOIN departments ON employees.dept_id = departments.id;

-- LEFT JOIN: Get all employees, show department if exists
SELECT employees.name, departments.dept_name
FROM employees
LEFT JOIN departments ON employees.dept_id = departments.id;

-- RIGHT JOIN: Get all departments, show employees if exist
SELECT employees.name, departments.dept_name
FROM employees
RIGHT JOIN departments ON employees.dept_id = departments.id;

-- FULL JOIN: Get all employees and departments
SELECT employees.name, departments.dept_name
FROM employees
FULL JOIN departments ON employees.dept_id = departments.id;

-- INNER JOIN with WHERE: Get high-paid employees with dept
SELECT e.name, e.salary, d.dept_name
FROM employees e
INNER JOIN departments d ON e.dept_id = d.id
WHERE e.salary > 60000;

-- Multiple JOINs: employees + departments + locations
SELECT e.name, d.dept_name, l.city
FROM employees e
INNER JOIN departments d ON e.dept_id = d.id
INNER JOIN locations l ON d.location_id = l.id;

-- LEFT JOIN with COUNT: departments with employee count
SELECT d.dept_name, COUNT(e.id) AS num_employees
FROM departments d
LEFT JOIN employees e ON d.id = e.dept_id
GROUP BY d.dept_name;
