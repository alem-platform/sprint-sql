# Optimal Way

| Expected file |
| ------------- |
| `optimal-way.sql` |

Marketing team needs data about our artists' performance. 

## Instructions:

Customer support team needs a detailed view of purchase patterns. Create a query that shows:

- Customer's full name (first name and last name delimited by single space) as `CustomerName`
- Their total number of **unique** purchases as `PurchaseCount`
- Their total spending as `TotalSpent`
- Average amount per purchase as `AveragePerPurchase`
- Date of their last purchase as `LastPurchaseDate`
- Date of their first purchase as `FirstPurchaseDate`
- How many different tracks they bought as `UniqueTrackCount`
- Their most expensive purchase amount as `LargestPurchase`

## Note:

- Round all money values to 2 decimal places
- Format dates using strftime to show as `'YYYY-MM-DD'`
- Order by total spent in descending order
- Only include customers with exactly 7 purchases

## Resources:

- [SQLite String Functions](https://www.sqlite.org/lang_corefunc.html)
- [SQLite Date Functions](https://www.sqlite.org/lang_datefunc.html)
- [SQLite Aggregate Functions](https://www.sqlite.org/lang_aggfunc.html)
- [SQLite HAVING](https://www.sqlitetutorial.net/sqlite-having/)
- [SQLite Subqueries](https://www.w3resource.com/sqlite/sqlite-subqueries.php)
- [SQLite ROUND Function](https://www.sqlite.org/lang_corefunc.html#round)
