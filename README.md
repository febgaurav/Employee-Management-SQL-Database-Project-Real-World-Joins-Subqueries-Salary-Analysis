# Employee-Management-SQL-Database-Project-Real-World-Joins-Subqueries-Salary-Analysis
SQL project demonstrating database design, joins, subqueries, aggregations, and employee salary analysis using MySQL.


# Company Database SQL Project

## Overview
This project demonstrates the creation and management of a relational database using MySQL.  
It includes database creation, table design, data insertion, joins, subqueries, and aggregate queries to analyze employee and department data.

The project simulates a simple company system that stores employee details, department information, salaries, and bonuses.

---

## Database Schema

The database **company** contains the following tables:

### 1. e_info
Stores employee basic information.

| Column | Type | Description |
|------|------|-------------|
| employee_ID | INT | Unique employee ID |
| employee_name | VARCHAR | Employee name |
| Division | VARCHAR | Department/Division |

---

### 2. Department
Stores department information.

| Column | Type | Description |
|------|------|-------------|
| dept_id | INT | Department ID |
| dept_name | VARCHAR | Department name |

---

### 3. salaries
Stores employee salary information.

| Column | Type | Description |
|------|------|-------------|
| employee_id | INT | Employee ID |
| salary | INT | Employee salary |

---

### 4. last_quarter_bonus
Stores employee bonus information.

| Column | Type | Description |
|------|------|-------------|
| employee_ID | INT | Employee ID |
| Bonus | INT | Bonus amount |

---

## Key SQL Concepts Used

This project demonstrates several SQL concepts including:

- Database creation
- Table creation
- ALTER TABLE
- INSERT statements
- INNER JOIN
- Aggregate functions (AVG, MAX, COUNT)
- Subqueries
- GROUP BY and HAVING
- Filtering with WHERE
- Case-insensitive joins using LOWER()

---

## Example Queries Included

### 1. Join Employees with Departments
Retrieves employees working in specific divisions.

```sql
SELECT *
FROM e_info AS E
JOIN Department AS D
ON E.division = D.dept_name
WHERE division IN ("logistic", "HR");
