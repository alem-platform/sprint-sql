# Sort Supreme

| Expected file |
| ------------- |
| `sort-supreme.sql` |

Elevate your sorting skills by mastering complex ORDER BY clauses.

### Instructions:

Using the `employees`, `departments`, and `products` tables, perform the following queries:

1. List all employees showing `first_name`, `last_name`, `salary`, and `department_id`, ordered by `department_id` ASC, `salary` DESC, and `last_name` ASC.

2. List departments showing `name`, `budget`, and `number_of_employees`, ordered by `number_of_employees` DESC, then by `name` ASC.
   - Calculate `number_of_employees` by counting employees in each department.

3. List products showing `name`, `price`, `rating`, and `quantity`, ordered by `rating` DESC, `price` ASC, and `quantity` DESC.

4. List employees hired in the last 5 years, showing `first_name`, `last_name`, `hire_date`, and `years_of_service`, ordered by `years_of_service` DESC, then by `hire_date` ASC.
   - Calculate `years_of_service` as the number of years since `hire_date`, rounded down to the nearest whole number.

### Resources:

- [SQL String Operations](https://www.sqlitetutorial.net/sqlite-string-functions/)

---