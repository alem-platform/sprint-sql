# Data Drop-In

| Expected file      |
| ------------------ |
| data-drop-in.sql |

Time to bring your table to life by inserting some data. Let's populate your `students` table with eager learners.

### Instructions:

- Insert the following records into the `students` table **right in this order**:

```
| student_id | first_name | last_name      | email                           | enrollment_date |
|------------|------------|----------------|---------------------------------|-----------------|
| 1          | Mustafa    | Sarvarov       | mustafa.sarvarov@gmail.com      | 2023-10-04      |
| 2          | Arthur     | Kim            | arthur.kim@alem.school          | 2024-10-04      |
| 3          | Elnar      | Moldabekov     | elnar.moldabekov@doodocs.net    | 2023-01-16      |
```

### Expected Result:

After executing your insert statement(s), the `students` table should contain three records corresponding to *Mustafa*, *Arthur*, and *Elnar*.

### Resources:

- [SQLite INSERT INTO Statement](https://www.sqlite.org/lang_insert.html)

### Facts: NULL vs Empty String
  - Unlike many other databases, SQLite treats an empty string (`''`) as different from `NULL`
  - This means INSERT INTO table(col) VALUES('') and `INSERT INTO table(col) VALUES(NULL)` store different values
  - Good to remember when working with `NOT NULL` constraints

