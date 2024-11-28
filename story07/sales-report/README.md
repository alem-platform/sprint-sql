# Sales Report

| Expected file |
| ------------- |
| `sales-report.sql` |

Track our monthly genre sales performance and find top-performing tracks.

### Instructions:

For each `YearAndMonth` and `Genre` **(name of the genre)** combination show sales data and find tracks that have equal number of purchases as the most purchased track in this `Genre` for this `YearAndMonth`.

Show:
- Year and month of `InvoiceDate` separated by `'-'` as `YearAndMonth`
- Genre name as it is
- Total amount for this `Genre/YearAndMonth` as `TotalSales`
- Number of unique customers as `UniqueCustomers`
- Average price per sale as `AveragePerSale`
- Name of track with most purchases as `TopTrack`

Note:
- Round all monetary values to 2 decimal points
- Group results by `YearAndMonth` and `Genre`
- Track must have same number of purchases as most purchased track (use subquery)
- Order by month descending, then by total sales descending

### Resources:
- [SQLite Date/Time Functions](https://www.sqlite.org/lang_datefunc.html)
- [SQLite Aggregate Functions](https://www.sqlite.org/lang_aggfunc.html)
- [SQLite Subqueries](https://www.w3resource.com/sqlite/sqlite-subqueries.php)
- [SQLite ROUND Function](https://www.sqlite.org/lang_corefunc.html#round)