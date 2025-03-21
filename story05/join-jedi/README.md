# New Database

Starting with this story, you will use a new database that closely resembles a real-world database.

Here is the schema of `week02.db` that you can find on [github](https://github.com/alem-platform/sprint-sql/blob/master/assets/week02.db):

## **Table: `artists`**

| Column Name | Data Type   | Constraints          |
|-------------|-------------|----------------------|
| `ArtistId`  | INTEGER     | PRIMARY KEY, AUTOINCREMENT |
| `Name`      | NVARCHAR(120) | NULLABLE          |

---

## **Table: `albums`**

| Column Name | Data Type   | Constraints                           |
|-------------|-------------|---------------------------------------|
| `AlbumId`   | INTEGER     | PRIMARY KEY, AUTOINCREMENT           |
| `Title`     | NVARCHAR(160) | NOT NULL                          |
| `ArtistId`  | INTEGER     | NOT NULL, FOREIGN KEY REFERENCES `artists(ArtistId)` |

### Index:
- `IFK_AlbumArtistId` on `ArtistId`

---

## **Table: `employees`**

| Column Name  | Data Type   | Constraints                           |
|--------------|-------------|---------------------------------------|
| `EmployeeId` | INTEGER     | PRIMARY KEY, AUTOINCREMENT           |
| `LastName`   | NVARCHAR(20) | NOT NULL                           |
| `FirstName`  | NVARCHAR(20) | NOT NULL                           |
| `Title`      | NVARCHAR(30) | NULLABLE                           |
| `ReportsTo`  | INTEGER     | FOREIGN KEY REFERENCES `employees(EmployeeId)` |
| `BirthDate`  | DATETIME    | NULLABLE                            |
| `HireDate`   | DATETIME    | NULLABLE                            |
| `Address`    | NVARCHAR(70) | NULLABLE                           |
| `City`       | NVARCHAR(40) | NULLABLE                           |
| `State`      | NVARCHAR(40) | NULLABLE                           |
| `Country`    | NVARCHAR(40) | NULLABLE                           |
| `PostalCode` | NVARCHAR(10) | NULLABLE                           |
| `Phone`      | NVARCHAR(24) | NULLABLE                           |
| `Fax`        | NVARCHAR(24) | NULLABLE                           |
| `Email`      | NVARCHAR(60) | NULLABLE                           |

### Index:
- `IFK_EmployeeReportsTo` on `ReportsTo`

---

## **Table: `customers`**

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

### Index:
- `IFK_CustomerSupportRepId` on `SupportRepId`

---

## **Table: `genres`**

| Column Name | Data Type     | Constraints          |
|-------------|---------------|----------------------|
| `GenreId`   | INTEGER       | PRIMARY KEY, AUTOINCREMENT |
| `Name`      | NVARCHAR(120) | NULLABLE            |

---

## **Table: `invoices`**

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

### Index:
- `IFK_InvoiceCustomerId` on `CustomerId`

---

## **Table: `media_types`**

| Column Name   | Data Type     | Constraints          |
|---------------|---------------|----------------------|
| `MediaTypeId` | INTEGER       | PRIMARY KEY, AUTOINCREMENT |
| `Name`        | NVARCHAR(120) | NULLABLE            |

---

## **Table: `playlists`**

| Column Name  | Data Type     | Constraints          |
|--------------|---------------|----------------------|
| `PlaylistId` | INTEGER       | PRIMARY KEY, AUTOINCREMENT |
| `Name`       | NVARCHAR(120) | NULLABLE            |

---

## **Table: `tracks`**

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

### Index:
- `IFK_TrackAlbumId` on `AlbumId`
- `IFK_TrackMediaTypeId` on `MediaTypeId`
- `IFK_TrackGenreId` on `GenreId`

---

## **Table: `invoice_items`**

| Column Name    | Data Type     | Constraints                           |
|----------------|---------------|---------------------------------------|
| `InvoiceLineId`| INTEGER       | PRIMARY KEY, AUTOINCREMENT           |
| `InvoiceId`    | INTEGER       | NOT NULL, FOREIGN KEY REFERENCES `invoices(InvoiceId)` |
| `TrackId`      | INTEGER       | NOT NULL, FOREIGN KEY REFERENCES `tracks(TrackId)` |
| `UnitPrice`    | NUMERIC(10,2) | NOT NULL                            |
| `Quantity`     | INTEGER       | NOT NULL                            |

### Index:
- `IFK_InvoiceLineInvoiceId` on `InvoiceId`
- `IFK_InvoiceLineTrackId` on `TrackId`

---

## **Table: `playlist_track`**

| Column Name  | Data Type     | Constraints                                |
|--------------|---------------|--------------------------------------------|
| `PlaylistId` | INTEGER       | NOT NULL, FOREIGN KEY REFERENCES `playlists(PlaylistId)` |
| `TrackId`    | INTEGER       | NOT NULL, FOREIGN KEY REFERENCES `tracks(TrackId)` |

### Composite Primary Key:
- `PlaylistId`, `TrackId`

### Index:
- `IFK_PlaylistTrackTrackId` on `TrackId`

---

<br>
<br>

# Join-Jedi

| Expected file |
| ------------- |
| `join-jedi.sql` |

Use your SQL skills to become a **Join-Jedi**! 

## Instructions:

Write a query that retrieves the `FirstName` and `LastName` of customers from the `Customers` table, along with their corresponding `InvoiceId` from the `Invoices` table. Only include customers who have made at least one purchase. 

Sort the result by `FirstName` in ascending order.

## Resources:

- [SQLite INNER JOIN](https://www.sqlitetutorial.net/sqlite-inner-join/)
- [One-to-Many Relationships](https://en.wikipedia.org/wiki/One-to-many_(data_model)/)
