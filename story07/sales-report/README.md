# Sales Report

| Expected file |
| ------------- |
| `sales-report.sql` |

Track our monthly genre sales performance with customer insights and sales share analysis.

## Instructions:

For each `YearAndMonth` and `Genre` combination, show sales data with the following metrics:

Show:
- Year and month of `InvoiceDate` separated by `'-'` as `YearAndMonth` (use *strftime*)
- Genre name as `Genre`
- Total amount for this Genre/YearAndMonth as `TotalSales` (rounded to 2 decimal points)
- Number of unique customers as `UniqueCustomers`
- Average price per sale as `AveragePerSale` (rounded to 2 decimal points)
- Number of tracks sold as `TracksSold`
- Percentage of total monthly sales as `GenreSharePercent` (rounded to 2 decimal points)

Requirements:
- Only include genres that have at least 2 unique customers in a given month
- Group result by `YearAndMonth` and `Genre`
- Order by `YearAndMonth` descending, then by `TotalSales` descending

## Resources:
- [SQLite Date/Time Functions](https://www.sqlite.org/lang_datefunc.html)
- [SQLite Aggregate Functions](https://www.sqlite.org/lang_aggfunc.html)
- [SQLite Subqueries](https://www.w3resource.com/sqlite/sqlite-subqueries.php)
- [SQLite ROUND Function](https://www.sqlite.org/lang_corefunc.html#round)
- [SQLite HAVING](https://www.sqlitetutorial.net/sqlite-having/)
