# Range Ranger

| Expected file |
| ------------- |
| `range-ranger.sql` |

Master BETWEEN and IN operators for efficient range queries.

### Instructions:

Using the `employees` table, create these queries:
1. Find employees with salary **BETWEEN** 4500 AND 5500
2. Find employees in departments with IDs IN (1, 3)
3. Find employees hired **BETWEEN** '2022-01-01' AND '2022-12-31'
4. Find employees with positions **IN** ('Developer', 'Senior Engineer', 'Lead Developer')

### Expected Result:

| first_name | last_name | salary  | position        | hire_date  |
|------------|-----------|---------|-----------------|------------|
| John       | Smith     | 5000.00 | Senior Engineer | 2021-03-15 |
| Sarah      | Williams  | 5500.00 | Senior Analyst  | 2022-03-15 |
[... matching employees ...]

### Resources:

- [SQL BETWEEN Operator](https://www.w3schools.com/sql/sql_between.asp)
- [SQL IN Operator](https://www.w3schools.com/sql/sql_in.asp)
- [SQL Date Functions](https://www.sqlite.org/lang_datefunc.html)

---