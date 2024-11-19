# Prefilled Database

Starting with this story, you will use prefilled database, as explained in the `hello-sql` task.

Here is the schema of `week01.db`:

### Employees Table

| Column Name   | Data Type     | Constraints                |
|---------------|---------------|----------------------------|
| employee_id   | INTEGER       | PRIMARY KEY AUTOINCREMENT  |
| first_name    | VARCHAR(50)   | NOT NULL                   |
| last_name     | VARCHAR(50)   | NOT NULL                   |
| email         | VARCHAR(100)  | NOT NULL UNIQUE            |
| salary        | DECIMAL(10,2) | NOT NULL                   |
| department_id | INT           | NOT NULL                   |
| position      | VARCHAR(100)  | NOT NULL                   |
| hire_date     | DATE          | NOT NULL                   |

### Departments Table

| Column Name  | Data Type     | Constraints               |
|--------------|---------------|---------------------------|
| department_id| INTEGER       | PRIMARY KEY AUTOINCREMENT |
| name         | VARCHAR(50)   | NOT NULL UNIQUE           |
| location     | VARCHAR(100)  | NOT NULL                  |
| budget       | DECIMAL(15,2) | NOT NULL                  |

### Products Table

| Column Name | Data Type    | Constraints                |
|-------------|--------------|----------------------------|
| product_id  | INTEGER      | PRIMARY KEY AUTOINCREMENT  |
| name        | VARCHAR(100) | NOT NULL                   |
| price       | DECIMAL(10,2)| NOT NULL                   |
| quantity    | INT          | NOT NULL                   |
| rating      | DECIMAL(3,2) | NOT NULL                   |

---

# Column Commander

| Expected file |
| ------------- |
| `column-commander.sql` |

Master the basics of column selection and manipulation.

### Instructions:

Using the `employees` table create three separate SELECT statements:
1. Select only `first_name` and `last_name` for employees in department_id 1
2. Select `email` as `contact_info` and `position` as `job_title` for employees who are "Senior Engineer"
3. Select `first_name`, `last_name`, and `salary`, but display `first_name` as `given_name` and `salary` as `monthly_income`

### Expected Result:

**Query 1:**
| first_name | last_name |
|------------|-----------|
| John       | Smith     |
| Mark       | Johnson   |
| Lisa       | Anderson  |

**Query 2:**
| contact_info         | job_title       |
|---------------------|-----------------|
| john.s@company.com  | Senior Engineer |
| james.w@company.com | Senior Engineer |

**Query 3:**
| given_name | last_name | monthly_income |
|------------|-----------|----------------|
| John       | Smith     | 5000.00        |
| Maria      | Garcia    | 6000.00        |
| Michael    | Brown     | 4500.00        |
[... rest of employees ...]


### Resources:

- [SQL Aliases](https://www.w3schools.com/sql/sql_alias.asp)
- [SQL WHERE Clause](https://www.w3schools.com/sql/sql_where.asp)

---