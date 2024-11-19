# Child In From

| Expected file |
| ------------- |
| `child-in-from.sql` |

Use a subquery in the `FROM` clause.

## Instructions:

Using the `products` table, write a query to find the ratings where the total quantity in stock exceeds 500 units. For these ratings, retrieve `rating`, the total quantity as `total_quantity`, and the average price as `average_price` (rounded to 2 decimal places).

## Expected Result:

| rating | total_quantity | average_price |
|--------|----------------|---------------|
| 4.50   | 770            | 76.49         |
| 4.40   | 530            | 42.37         |


## Resources:

- [SQLite Subqueries](https://www.sqlite.org/lang_select.html#subqueries)
- [SQLite Aggregate Functions](https://www.sqlite.org/lang_aggfunc.html)
- [SQLite GROUP BY clause](https://www.sqlite.org/lang_select.html#groupby)