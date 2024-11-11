# Sort Supreme

| Expected file |
| ------------- |
| `sort-supreme.sql` |

Master various sorting techniques using ORDER BY.

### Instructions:

Create these queries using `employees` and `departments` tables:
1. List all employees ordered by salary DESC, then by last_name ASC
2. List departments ordered by budget DESC, showing department name and budget
3. List employees ordered by hire_date DESC, showing only those hired in 2023
4. List all products ordered by rating DESC, then by price ASC

### Expected Result:

Query 1:
| first_name | last_name | salary  |
|------------|-----------|---------|
| Maria      | Garcia    | 6000.00 |
| James      | Wilson    | 5800.00 |
[... rest in salary DESC, last_name ASC order ...]

Query 2:
| name        | budget     |
|-------------|------------|
| Engineering | 1000000.00 |
| Development | 800000.00  |
[... rest in budget DESC order ...]