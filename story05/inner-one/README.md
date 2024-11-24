# Inner One

| Expected file |
| ------------- |
| `inner-one.sql` |

Utilize the power of joins to retrieve detailed information across the database. 

## Instructions:

Write a query that:
1. Retrieves the `EmployeeName` that consists of employee's first and last names separted by space.
2. Retrieves the `CustomerName` that consists of customer's first and last names separted by space.
3. Includes the `InvoiceId` and `InvoiceDate`.
4. Retrieves details about purchased tracks: 
   - Track name as `TrackName`.
   - Album title as `AlbumTitle`.
   - Artist name as `ArtistName`.
   - Genre name as `GenreName`.
   - Media type name as `MediaTypeName`.
   - Filters the results to include only customers assigned to a support representative (`SupportRepId` matches `EmployeeId`).
6. Sorts the results by `EmployeeName`, `CustomerName`, and `InvoiceDate` in ascending order.

## Resources:

- [SQLite INNER JOIN](https://www.sqlitetutorial.net/sqlite-inner-join/)
- [Joining Tables in SQL](https://www.w3schools.com/sql/sql_join_inner.asp)

---