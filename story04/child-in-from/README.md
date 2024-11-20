# Child In From

| Expected file |
| ------------- |
| `child-in-from.sql` |

## Instructions:

Write a query using a subquery in the FROM clause that:
1. First creates a derived table containing rating, total quantity, and average price for all ratings
2. Then selects from this derived table to find ratings where total quantity exceeds 500 units

Using the `products` table, retrieve `rating`, the total quantity as `total_quantity`, and the average price as `average_price` (rounded to 2 decimal places).

**Note:** The solution MUST use a subquery in the FROM clause.

## Resources:

- [SQLite Subqueries](https://www.sqlite.org/lang_select.html#subqueries)
- [SQLite Aggregate Functions](https://www.sqlite.org/lang_aggfunc.html)
- [SQLite GROUP BY clause](https://www.sqlite.org/lang_select.html#groupby)