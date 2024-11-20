# Anything And Everything

| Expected file |
| ------------- |
| `anything-and-everything.sql` |

## Instructions:

Using the `products` table:
1. Write a query to find products that have a price higher than **ANY** product with a rating of 4.8 (meaning higher than at least one such product). Retrieve `product_id`, `name`, and `price`.
2. Write a query to find products that have a price higher than **ALL** products with a rating of 4.8 (meaning higher than every such product). Retrieve `product_id`, `name`, and `price`.

Note: Since SQLite doesn't support ANY and ALL operators directly, come up with ways to simulate them.

## Resources:

- [SQL ANY and ALL Operators](https://www.w3schools.com/sql/sql_any_all.asp)
- [SQLite Subqueries](https://www.sqlite.org/lang_select.html#subqueries)
- [SQLite Comparison Operators](https://www.sqlite.org/lang_expr.html#binaryops)