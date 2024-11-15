# Grouped Calculations

| Expected file |
| ------------- |
| `grouped-calculations.sql` |

Compute aggregate values with grouped data.

## Instructions:

Using the `products` table, write a query to find the average price and total quantity of products for each rating. Retrieve `rating`, average price as `avg_price`, and total quantity as `total_quantity`, ordered by `rating` descending.

## Expected Result:

| rating | avg_price | total_quantity |
|--------|-----------|----------------|
| 4.80   | 199.50    | 60             |
| 4.70   | 159.99    | 70             |
[... etc ...]

## Resources:

- [SQL GROUP BY Statement - W3Schools](https://www.w3schools.com/sql/sql_groupby.asp)
- [Aggregate Functions with GROUP BY - SQL Tutorial](https://www.sqltutorial.org/sql-group-by/)
- [MySQL Aggregate Functions](https://dev.mysql.com/doc/refman/8.0/en/group-by-functions.html)
