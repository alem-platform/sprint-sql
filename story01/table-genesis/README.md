# Table Genesis

| Expected file  |
| -------------- |
| `table-genesis.sql` |

Every database begins with tables. Your journey starts by creating your very first table. Let's set the foundation for our data adventure!

### Instructions:

- The table should have the following columns:

```
| Column Name      | Data Type     | Constraints                     |
|-------------------|--------------|---------------------------------|
| `student_id`      | INTEGER      | PRIMARY KEY                     |
| `first_name`      | TEXT         | NOT NULL                        |
| `last_name`       | TEXT         | NOT NULL                        |
| `email`           | TEXT         | NOT NULL, UNIQUE                |
| `enrollment_date` | DATE         | NOT NULL                        |
```

- Write a SQL query to create a table named `students`.

### Expected Result:

After running your SQL script, the table `students` should be created with the specified columns and constraints.

### Resources:

- [SQLite CREATE TABLE Statement](https://www.sqlite.org/lang_createtable.html)
- [SQLite Data Types](https://www.sqlite.org/datatype3.html)

### Facts: Type Affinity in SQLite

In most databases you would see the basic data types as *integer*, *text*, *date* and etc. But every database implements them in their own way and it's very useful to know how particular database does that. For example, SQLite [converts](https://www.sqlite.org/datatype3.html#date_and_time_datatype:~:text=CHARACTER(20),2) any column type that has *CHAR*, *CLOB*, *TEXT* to *TEXT* type
