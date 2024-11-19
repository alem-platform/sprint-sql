# Data Analyst Dilemma

| Expected file |
| ------------- |
| `data-analyst-dilemma.sql` |

Perform advanced aggregate calculations and analyze data trends.

## Instructions:

Using the `products` table, write a query to find the rating groups where:

- The total inventory value (sum of `price * quantity`) is greater than 20,000.
- The group's average rating is less than the overall average rating of all products.

Retrieve `rating`, total inventory value as `total_inventory_value`, and average rating as `average_rating`, ordered by `total_inventory_value` descending.

## Resources:

- [SQLite Aggregate Functions](https://www.sqlite.org/lang_aggfunc.html)
- [SQLite HAVING Clause](https://www.sqlite.org/lang_select.html#the_having_clause)
- [SQLite Arithmetic Operators](https://www.sqlite.org/lang_expr.html#operators)
- [SQLite Subqueries](https://www.sqlite.org/lang_select.html#subqueries)
