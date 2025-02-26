# customer-artist

| Expected file |
| ------------- |
| `customer-artist.sql` |

Find customers' favorite artists based on purchase history.

For each customer and artist combination (customer and artist ids) calculate:
1. How many of artist's tracks customer bought
2. Total amount spent on this artist's tracks
3. What percentage of customer's total purchases these tracks represent
4. Number of **unique** albums bought from

Then show:
- Customer's full name (first and last names separated by single space) as `Customer`
- Artist name as `ArtistName`
- Number of tracks bought as `TrackCount`
- Total spent on artist as `TotalSpent`, rounded to 2 decimal places
- Percentage of all purchases as `Percentage`, rounded to 1 decimal place
- Number of **unique** albums as `AlbumCount`

Where:
- Only include customers who spent more than `$40` in total
- Only show artists that make up more than `5%` of customer's purchases

Note:
- Calculate total spent as UnitPrice × Quantity from invoice_items
- Sort the result by customer name in ascending order, then by total spent descending order

# Table: `artists`

```
| Column Name | Data Type   | Constraints          |
|-------------|-------------|----------------------|
| `ArtistId`  | INTEGER     | PRIMARY KEY, AUTOINCREMENT |
| `Name`      | NVARCHAR(120) | NULLABLE          |
```

# Table: `albums`

```
| Column Name | Data Type   | Constraints                           |
|-------------|-------------|---------------------------------------|
| `AlbumId`   | INTEGER     | PRIMARY KEY, AUTOINCREMENT           |
| `Title`     | NVARCHAR(160) | NOT NULL                          |
| `ArtistId`  | INTEGER     | NOT NULL, FOREIGN KEY REFERENCES `artists(ArtistId)` |
```

# Table: `customers`

```
| Column Name   | Data Type     | Constraints                           |
|---------------|---------------|---------------------------------------|
| `CustomerId`  | INTEGER       | PRIMARY KEY, AUTOINCREMENT           |
| `FirstName`   | NVARCHAR(40)  | NOT NULL                            |
| `LastName`    | NVARCHAR(20)  | NOT NULL                            |
| `Company`     | NVARCHAR(80)  | NULLABLE                            |
| `Address`     | NVARCHAR(70)  | NULLABLE                            |
| `City`        | NVARCHAR(40)  | NULLABLE                            |
| `State`       | NVARCHAR(40)  | NULLABLE                            |
| `Country`     | NVARCHAR(40)  | NULLABLE                            |
| `PostalCode`  | NVARCHAR(10)  | NULLABLE                            |
| `Phone`       | NVARCHAR(24)  | NULLABLE                            |
| `Fax`         | NVARCHAR(24)  | NULLABLE                            |
| `Email`       | NVARCHAR(60)  | NOT NULL                            |
| `SupportRepId`| INTEGER       | FOREIGN KEY REFERENCES `employees(EmployeeId)` |
```

# Table: `invoices`

```
| Column Name        | Data Type     | Constraints                           |
|--------------------|---------------|---------------------------------------|
| `InvoiceId`        | INTEGER       | PRIMARY KEY, AUTOINCREMENT           |
| `CustomerId`       | INTEGER       | NOT NULL, FOREIGN KEY REFERENCES `customers(CustomerId)` |
| `InvoiceDate`      | DATETIME      | NOT NULL                            |
| `BillingAddress`   | NVARCHAR(70)  | NULLABLE                            |
| `BillingCity`      | NVARCHAR(40)  | NULLABLE                            |
| `BillingState`     | NVARCHAR(40)  | NULLABLE                            |
| `BillingCountry`   | NVARCHAR(40)  | NULLABLE                            |
| `BillingPostalCode`| NVARCHAR(10)  | NULLABLE                            |
| `Total`            | NUMERIC(10,2) | NOT NULL                            |
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
