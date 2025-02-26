# employee-profile

| Expected file             |
| ------------------------- |
| `employee-profile.sql`        |

Display employee's contact information where show their:

- last name
- email 
- country

Sort result by last name in ascending order

# Table: `employees`

```
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
```