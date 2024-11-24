# Foreigner

| Expected file |
| ------------- |
| `foreigner.sql` |

As a **Foreigner** navigating a unfamilliar database, explore it and its data

## Instructions:

Write several queries by these tasks:
1. Retrieve customer(s) along with their support representatives (`CustomerId`, Customers first and last names as `CustomerName`, Employees first and last names as `SupportRepName` and Employees title as `SupportRepTitle`). Sort the result by `CustomerName` in ascending order.
2. Retrieve invoices along with their customers (`InvoiceId`, `InvoiceDate`, Customers first and last names as `CustomerName`). Sort the result by `CustomerName` in descending order.
3. Retrieve tracks with their album titles and corresponding artist names (`TrackId`, Track's name as `TrackName`, Album's title as `AlbumTitle`, Artist's name as `ArtistName`). Sort the result by `TrackName` in descending order.
4. Retrieve invoice items along with track names, album titles, and artist names (`InvoiceLineId`, Track's name as `TrackName`, Album's title as `AlbumTitle`, Artist's name as `ArtistName`). Sort the result by `AlbumTitle` in ascending order.

## Resources:

- [SQLite Foreign Key Constraints](https://www.sqlite.org/foreignkeys.html)
- [SQLite INNER JOIN](https://www.geeksforgeeks.org/sqlite-joins/)

---