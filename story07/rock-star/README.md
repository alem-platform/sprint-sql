# week02.db schema

It's [here](https://github.com/alem-platform/sprint-sql/blob/master/assets/week02.db)

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

# Rock Star

| Expected file |
| ------------- |
| `rock-star.sql` |

Time to give rock stars their own VIP table!

## Instructions:

Create a comprehensive `rock_stars` table that captures the essence of musical legends with the following specifications:

1. **Basic Identification**
   - `RockStarId`: Primary key, auto-increment
   - `StageName`: Text, required, unique
   - `BandName`: Optional text field

2. **Career Metrics**
   - `YearsActive`: Integer with range constraint (from 1 to 70 inclusive), default value to 1
   - `GuitarBrandPreference`: Predefined guitar brand preference text field that **must be** one from next list: ( 'Fender', 'Gibson', 'Ibanez', 'PRS', 'Gretsch', 'ESP', 'Jackson', 'Other')

3. **Financial Tracking**
   - `MonthlyRoyalties`: Decimal for precise earnings 
     * 8 characters long 
     * 2 digits after decimal point
     * Non-negative values
     * Default value is zero
     * Optional

4. **Career Timestamps**
   - `CareerStartDate`: **Date** of first professional performance
     * Default value is current time
     * Required

5. **Foreign Key Relationships**:
    - Link to `artists` table via `ArtistId`
    - Link to `genres` table via `GenreId`
    - Both are required

## Resources:
- [SQLite CREATE TABLE](https://www.sqlitetutorial.net/sqlite-create-table/)
- [SQLite Constraints](https://www.tutorialspoint.com/sqlite/sqlite_constraints.htm)
- [SQLite CHECK](https://www.sqlitetutorial.net/sqlite-check-constraint/)
