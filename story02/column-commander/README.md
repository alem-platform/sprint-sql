# Prefilled Database

Starting with this story, you will use prefilled database, as explained in the `hello-sql` task.

Here is the schema of `week01.db` that you can find on [github](https://github.com/alem-platform/sprint-sql/blob/master/assets/week01.db):

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

# Column Commander

| Expected file |
| ------------- |
| `column-commander.sql` |

Master the basics of column selection and manipulation.

### Instructions:

Using the `employees` table create three separate SELECT statements:
1. Select only `first_name` and `last_name` for employees in department_id 1. Sort it by first name in ascending order.
2. Select `email` as *contact_info* and `position` as *job_title* for employees who are "Lead Engineer"
3. Select `first_name` and `last_name` as *given_name* and `salary` as *monthly_income*. Sort it by monthly income in descending order and then by given name in ascending order.

### Resources:

- [SQL Aliases](https://www.w3schools.com/sql/sql_alias.asp)
- [SQL WHERE Clause](https://www.w3schools.com/sql/sql_where.asp)
