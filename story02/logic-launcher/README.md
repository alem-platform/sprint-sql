# Logic Launcher

| Expected file |
| ------------- |
| `logic-launcher.sql` |

Apply logical operators to create complex conditions.

### Instructions:

Using the `employees` and `departments` tables, create queries to find:
1. Engineers (any position containing 'Engineer') with salary > 5000 
2. Employees in Engineering OR Development departments (use department names)
3. Employees NOT in Analytics department who make more than 5000
4. Developers hired in 2023 with salary less than 5000

### Expected Result:

| first_name | last_name | position        | salary  | department_name |
|------------|-----------|-----------------|---------|-----------------|
| John       | Smith     | Senior Engineer | 5000.00 | Engineering     |
| James      | Wilson    | Senior Engineer | 5800.00 | Development     |
[... more matching employees ...]


### Resources:

- [SQL Logical Operators](https://www.w3schools.com/sql/sql_and.asp)
- [SQL IN Operator](https://www.w3schools.com/sql/sql_in.asp)
- [SQL NOT Operator](https://www.w3schools.com/sql/sql_not.asp)
- [SQL LIKE Operator](https://www.w3schools.com/sql/sql_like.asp)

---