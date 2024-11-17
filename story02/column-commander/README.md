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