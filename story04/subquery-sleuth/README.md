# week01.db schema

Also, notice that you can't use `JOIN` in this story, try to solve next tasks with subqueries only.

### Employees Table

| Column Name   | Data Type     | Constraints                |
|---------------|---------------|----------------------------|
| employee_id   | INTEGER       | PRIMARY KEY AUTOINCREMENT  |
| first_name    | TEXT          | NOT NULL                   |
| last_name     | TEXT          | NOT NULL                   |
| email         | TEXT          | NOT NULL UNIQUE            |
| salary        | REAL          | NOT NULL                   |
| department_id | INTEGER       | NOT NULL                   |
| position      | TEXT          | NOT NULL                   |
| hire_date     | TEXT          | NOT NULL                   |

### Departments Table

| Column Name  | Data Type     | Constraints               |
|--------------|---------------|---------------------------|
| department_id| INTEGER       | PRIMARY KEY AUTOINCREMENT |
| name         | TEXT          | NOT NULL UNIQUE           |
| location     | TEXT          | NOT NULL                  |
| budget       | REAL          | NOT NULL                  |

### Products Table

| Column Name | Data Type    | Constraints                |
|-------------|--------------|----------------------------|
| product_id  | INTEGER      | PRIMARY KEY AUTOINCREMENT  |
| name        | TEXT         | NOT NULL                   |
| price       | REAL         | NOT NULL                   |
| quantity    | INTEGER      | NOT NULL                   |
| rating      | REAL         | NOT NULL                   |

---

# Subquery Sleuth

| Expected file |
| ------------- |
| `subquery-sleuth.sql` |

## Instructions:

Using the `employees` and `departments` tables, write a query to find the first and last names of employees who work in the department with the highest budget. Sort the result by `first_name`.

## Resources:

- [SQLite Subqueries](https://www.sqlitetutorial.net/sqlite-subquery/)