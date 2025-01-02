# week01.db schema

It's [here](https://github.com/alem-platform/sprint-sql/blob/master/assets/week01.db)

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

# Distinct Detective

| Expected file |
| ------------- |
| `distinct-detective.sql` |

## Instructions:

Using the `employees` table, write a query to retrieve all the unique `positions` held by employees.
Sort the result by `position` in descending order.

## Resources:

- [SQLite SELECT DISTINCT](https://www.sqlitetutorial.net/sqlite-distinct/)
