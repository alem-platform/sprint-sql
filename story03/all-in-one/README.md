# All In One

| Expected file |
| ------------- |
| `all-in-one.sql` |

Use combined filtering conditions with `WHERE`, `GROUP BY`, and `HAVING`.

## Instructions:

Using the `employees` table, write a query to find departments where:

- The average salary is greater than 10,000.
- The maximum salary is less than 1,000,000.
- Only consider employees in positions that contain the word **'Engineer'** or **'Manager'**.

Retrieve `department_id`, average salary rounded to a whole number as `average_salary`, and maximum salary as `max_salary`, ordered by `max_salary` in a descending order.

## Resources:

- [SQLite WHERE Clause](https://www.sqlite.org/lang_expr.html#the_where_clause)
- [SQLite GROUP BY Clause](https://www.sqlite.org/lang_select.html#groupby)
- [SQLite HAVING Clause](https://www.sqlite.org/lang_select.html#the_having_clause)
- [SQLite MAX() Function](https://www.sqlite.org/lang_aggfunc.html#max)
