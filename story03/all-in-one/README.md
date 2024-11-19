# All In One

| Expected file |
| ------------- |
| `all-in-one.sql` |

Use combined filtering conditions with `WHERE`, `GROUP BY`, and `HAVING`.

## Instructions:

Using the `employees` table, write a query to find departments where:

- The average salary is greater than 40,000.
- The maximum salary is less than 120,000.
- Only consider employees in positions that contain the word **'Engineer'**.

Retrieve `department_id`, average salary as `average_salary`, and maximum salary as `max_salary`, ordered by `department_id`.

## Resources:

- [SQLite WHERE Clause](https://www.sqlite.org/lang_expr.html#the_where_clause)
- [SQLite GROUP BY Clause](https://www.sqlite.org/lang_select.html#groupby)
- [SQLite HAVING Clause](https://www.sqlite.org/lang_select.html#the_having_clause)
- [SQLite MAX() Function](https://www.sqlite.org/lang_aggfunc.html#max)
