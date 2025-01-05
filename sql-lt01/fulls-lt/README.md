# fulls-lt

| Expected file             |
| ------------------------- |
| `fulls-lt.sql`        |

Retrieve customers' first and last names separated by single space as `FullName`.

Sort the result by `FullName` in ascending order

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