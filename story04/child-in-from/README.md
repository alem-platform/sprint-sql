# Child In From

| Expected file |
| ------------- |
| `child-in-from.sql` |

Use a subquery in the `FROM` clause.

## Instructions:

Using the `products` table, write a query to find the ratings where the total quantity in stock exceeds 500 units. For these ratings, retrieve `rating`, the total quantity as `total_quantity`, and the average price as `average_price`.

## Expected Result:

| rating | total_quantity | average_price |
|--------|----------------|---------------|
| 4.50   | 770            | 76.49         |
| 4.40   | 530            | 42.37         |

## Resources:

- [Subqueries in the FROM Clause](https://www.w3schools.com/sql/sql_subqueries.asp)
- [Subquery Factoring in FROM Clause - Oracle Documentation](https://docs.oracle.com/database/121/SQLRF/statements_10002.htm#SQLRF52363)
- [MySQL Derived Tables (Subqueries in FROM Clause)](https://dev.mysql.com/doc/refman/8.0/en/derived-tables.html)
