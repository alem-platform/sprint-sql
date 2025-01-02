# Data Analyst Dilemma

| Expected file |
| ------------- |
| `data-analyst-dilemma.sql` |

Perform advanced aggregate calculations and analyze data trends.

## Instructions:

Using the `products` table, write a query to find the rating groups where:

- The total inventory value (sum of `price * quantity`) is greater than 20,000.
- The group's average rating is less than: the overall average rating of all products + 50,000.

Retrieve `rating`, total inventory value as `total_inventory_value`, and average rating rounded to one decimal place as `average_rating`, ordered by `total_inventory_value` descending.

## Resources:

- [SQLite Aggregate Functions](https://www.sqlite.org/lang_aggfunc.html)
- [SQLite Subqueries](https://www.sqlitetutorial.net/sqlite-subquery/)
