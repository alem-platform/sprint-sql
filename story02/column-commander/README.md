# Column Commander

| Expected file |
| ------------- |
| `column-commander.sql` |

Master the basics of column selection and manipulation.

### employees
| Column Name     | Data Type      | Constraints                 |
|----------------|----------------|----------------------------|
| `employee_id`   | INT           | PRIMARY KEY, AUTO_INCREMENT |
| `first_name`    | VARCHAR(50)   | NOT NULL                    |
| `last_name`     | VARCHAR(50)   | NOT NULL                    |
| `email`         | VARCHAR(100)  | NOT NULL, UNIQUE            |
| `salary`        | DECIMAL(10,2) | NOT NULL                    |
| `department_id` | INT           | NOT NULL                    |
| `position`      | VARCHAR(100)  | NOT NULL                    |
| `hire_date`     | DATE         | NOT NULL                    |

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