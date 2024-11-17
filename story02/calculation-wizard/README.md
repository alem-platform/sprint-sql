# Calculation Wizard

| Expected file |
| ------------- |
| `calculation-wizard.sql` |

Practice creating calculated columns using mathematical operations.

### Instructions:

Using the `employees` table, create a query that shows:
1. `first_name` and `last_name` combined with a space as `full_name`
2. `salary` multiplied by 12 as `annual_salary`
3. `salary` increased by 10% as `increased_salary`
4. Number of years since `hire_date` as `years_employed`
5. `salary` divided by 20 as `daily_rate` (assuming 20 working days per month)

### Expected Result:

| full_name      | annual_salary | increased_salary | years_employed | daily_rate |
|----------------|---------------|------------------|----------------|------------|
| John Smith     | 60000.00      | 5500.00          | 3             | 250.00     |
| Maria Garcia   | 72000.00      | 6600.00          | 3             | 300.00     |
[... rest of employees ...]

### Resources:

- [SQL Functions](https://www.w3schools.com/sql/sql_ref_sqlserver.asp)
- [SQL Operators](https://www.w3schools.com/sql/sql_operators.asp)
- [SQL Date Functions](https://www.sqlite.org/lang_datefunc.html)

---