# Sales Report

| Expected file |
| ------------- |
| `sales-report.sql` |

Track our monthly sales performance by genre. 

### Instructions:

Write a query to show:
- Year and month of the sale delimited by `'-'` as `YearAndMonth`
- Genre name as it is
- Total sales amount for this genre in this month as `TotalSales`
- Number of unique customers who bought tracks of this genre that month as `UniqueCustomers`
- Average unit price for tracks in this genre for this month as `AveragePerSale`
- Most purchased track name in this genre for this month as `TopTrack`

Note:
- Round monetary values (`TotalSales`, `AveragePerSale`) to 2 decimal places
- Group results by `YearAndMonth` and genre
- Find the track with most purchases in each genre-month combination
- Order by month descending, then by total sales descending

### Resources:
- [SQLite Date/Time Functions](https://www.sqlite.org/lang_datefunc.html)
- [SQLite Aggregate Functions](https://www.sqlite.org/lang_aggfunc.html)
- [SQLite Subqueries](https://www.w3resource.com/sqlite/sqlite-subqueries.php)
- [SQLite ROUND Function](https://www.sqlite.org/lang_corefunc.html#round)