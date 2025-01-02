# Child In From

| Expected file |
| ------------- |
| `child-in-from.sql` |

## Instructions:

Write a query using a subquery in the *FROM* clause that:
1. First create a subquery containing rating, total quantity, and average price for all ratings:
    - Using the `products` table, retrieve `rating`, the total quantity as `total_quantity`, and the average price as `average_price` (rounded to 2 decimal places).
2. Then select from this derived table to find ratings where total quantity exceeds 500 units
3. Sort the result in descending order by `rating` column of subquery

## Note:

The solution MUST use a subquery in the FROM clause

## Resources:

- [SQLite Subqueries](https://www.sqlitetutorial.net/sqlite-subquery/)
- [SQLite Aggregate Functions](https://www.sqlite.org/lang_aggfunc.html)
- [SQLite GROUP BY clause](https://www.sqlitetutorial.net/sqlite-group-by/)