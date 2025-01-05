# Premium Ones

| Expected file |
| ------------- |
| `premium-ones.sql` |

The bests among others

## Instructions:

Help our marketing identify premium tracks that match specific criteria. Find all tracks that are:
- Longer than 5 minutes
- Priced above average for their genre
- Have been purchased at least two times
- Are not in the 'Heavy Metal' genre

For each track show:
- Track name as `TrackName`
- Track length in seconds as `Seconds`
- Track's unit price as `TrackPrice`
- Genre name as `GenreName`
- Number of times this track was purchased as `PurchaseCount`

Note:
- There is 60,000 milliseconds in one minute
- Compare track price with average price in its genre using subquery
- Sort the result by number of purchases in descending order, then by tracks unit price in descending order

## Resources:
- [SQLite Comparison Operators](https://www.sqlite.org/lang_expr.html)
- [SQLite Aggregate Functions](https://www.sqlite.org/lang_aggfunc.html)
- [SQLite Subqueries](https://www.w3resource.com/sqlite/sqlite-subqueries.php)
- [SQLite HAVING](https://www.sqlitetutorial.net/sqlite-having/)

# Table: `genres`

```
| Column Name | Data Type     | Constraints          |
|-------------|---------------|----------------------|
| `GenreId`   | INTEGER       | PRIMARY KEY, AUTOINCREMENT |
| `Name`      | NVARCHAR(120) | NULLABLE            |
```

# Table: `tracks`

```
| Column Name    | Data Type     | Constraints                           |
|----------------|---------------|---------------------------------------|
| `TrackId`      | INTEGER       | PRIMARY KEY, AUTOINCREMENT           |
| `Name`         | NVARCHAR(200) | NOT NULL                            |
| `AlbumId`      | INTEGER       | FOREIGN KEY REFERENCES `albums(AlbumId)` |
| `MediaTypeId`  | INTEGER       | NOT NULL, FOREIGN KEY REFERENCES `media_types(MediaTypeId)` |
| `GenreId`      | INTEGER       | FOREIGN KEY REFERENCES `genres(GenreId)` |
| `Composer`     | NVARCHAR(220) | NULLABLE                            |
| `Milliseconds` | INTEGER       | NOT NULL                            |
| `Bytes`        | INTEGER       | NULLABLE                            |
| `UnitPrice`    | NUMERIC(10,2) | NOT NULL                            |
```

# Table: `invoice_items`

```
| Column Name    | Data Type     | Constraints                           |
|----------------|---------------|---------------------------------------|
| `InvoiceLineId`| INTEGER       | PRIMARY KEY, AUTOINCREMENT           |
| `InvoiceId`    | INTEGER       | NOT NULL, FOREIGN KEY REFERENCES `invoices(InvoiceId)` |
| `TrackId`      | INTEGER       | NOT NULL, FOREIGN KEY REFERENCES `tracks(TrackId)` |
| `UnitPrice`    | NUMERIC(10,2) | NOT NULL                            |
| `Quantity`     | INTEGER       | NOT NULL                            |
```
