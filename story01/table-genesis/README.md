# Table Genesis

| Expected file        |
| -------------------- |
| table-genesis.sql |

Every database begins with tables. Your journey starts by creating your very first table. Let's set the foundation for our data adventure!

### Instructions:

- The table should have the following columns:

| Column Name      | Data Type     | Constraints                     |
|-------------------|--------------|---------------------------------|
| `student_id`      | INT          | PRIMARY KEY     |
| `first_name`      | VARCHAR(50)  | NOT NULL                        |
| `last_name`       | VARCHAR(50)  | NOT NULL                        |
| `email`           | VARCHAR(100) | NOT NULL, UNIQUE                |
| `enrollment_date` | DATE         | NOT NULL                        |

- Write a SQL query to create a table named `students`.

### Resources:

- [SQL CREATE TABLE Statement](https://www.w3schools.com/sql/sql_create_table.asp)
- [SQL Data Types](https://www.w3schools.com/sql/sql_datatypes.asp)

### Expected Result:

After running your SQL script, the table `students` should be created with the specified columns and constraints.

---
