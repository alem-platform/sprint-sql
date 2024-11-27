# Premium Ones

| Expected file |
| ------------- |
| `premium-ones.sql` |

The bests among others

### Instructions:

Help our marketing identify premium tracks that match specific criteria. Find all tracks that are:
- Longer than 5 minutes
- Priced above average for their genre
- Have been purchased at least two times
- Are not in the 'Heavy Metal' genre

For each track show:
- Track name as it is
- Track length in seconds as `Seconds`
- Track's unit price as it is
- Genre name as it is
- Number of times this track was purchased as `PurchaseCount`

Note:
- Compare track price with average price in its genre using subquery
- Order results by number of purchases descending, then by track price descending

### Resources:
- [SQLite Comparison Operators](https://www.sqlite.org/lang_expr.html)
- [SQLite Aggregate Functions](https://www.sqlite.org/lang_aggfunc.html)
- [SQLite Subqueries](https://www.w3resource.com/sqlite/sqlite-subqueries.php)
