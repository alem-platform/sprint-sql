# Case Constructor

| Expected file |
| ------------- |
| `case-constructor.sql` |

Learn to apply conditional logic using CASE expressions.

### Instructions:

Using the `employees` table, create a query showing:
1. `full_name` (combine `first_name` and `last_name`).
2. Salary category:
   - Above 75,000: 'High'
   - 50,000–75,000: 'Medium'
   - Below 50,000: 'Low'.
3. Employee type based on `department_id`:
   - Department 1–5: 'Core Team'
   - Department 6–10: 'Support Team'.

### Expected Result:

| full_name      | salary_category | employee_type |
|----------------|-----------------|---------------|
| Emma Clark     | High            | Core Team     |
| Liam Johnson   | High            | Core Team     |
| Olivia Williams| Medium          | Support Team  |
[... rest of employees ...]

### Resources:

- [SQL CASE Expression](https://www.w3schools.com/sql/sql_case.asp)

---