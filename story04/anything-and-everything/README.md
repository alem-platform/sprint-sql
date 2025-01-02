# Anything And Everything

| Expected file |
| ------------- |
| `anything-and-everything.sql` |

## Instructions:

Using the `products` table:
1. Write a query to find products that have a price higher than **ANY** product with a rating between 4.5 and 4.6.
2. Write a query to find products that have a price higher than **ALL** products with a rating between 4.1 and 4.2.

In all queries retrieve product's id, name and price. Sort the output by `price` in descending order.

## Note:

Since SQLite doesn't support ANY and ALL operators directly, come up with ways to simulate them.

## Resources:

- [SQL ANY and ALL Operators](https://www.w3schools.com/sql/sql_any_all.asp)
- [SQLite Subqueries](https://www.sqlitetutorial.net/sqlite-subquery/)
- [SQLite Comparison Operators](https://www.sqlite.org/lang_expr.html#binaryops)