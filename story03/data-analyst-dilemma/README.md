# Data Analyst Dilemma

| Expected file |
| ------------- |
| `data-analyst-dilemma.sql` |

Perform advanced aggregate calculations and analyze data trends.

## Instructions:

Using the `products` table, write a query to find the rating groups where:

- The total inventory value (sum of `price * quantity`) is greater than 50,000.
- The group's average rating is less than the overall average rating of all products.

Retrieve `rating`, total inventory value as `total_inventory_value`, and average rating as `average_rating`, ordered by `total_inventory_value` descending.

## Resources:

- [SQL Aggregate Functions](https://www.w3schools.com/sql/sql_count_avg_sum.asp)
- [Subqueries in HAVING Clause](https://www.sqltutorial.org/sql-having/)
- [SQL Arithmetic Operators](https://www.w3schools.com/sql/sql_operators.asp)
- [Using Subqueries in SQL](https://www.datacamp.com/community/tutorials/sql-subqueries-tutorial)
