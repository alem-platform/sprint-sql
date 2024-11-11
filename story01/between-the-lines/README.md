# Between the Lines

| Expected file        |
| -------------------- |
| `between-the-lines.sql` |

Use `BETWEEN` and `IN` to specify ranges and specific values. Read between the lines to find your data.

### Instructions:

- **Part A:** Select `first_name`, `last_name` of students with a `test_score` **between** 80 and 90.
- **Part B:** Select `first_name`, `last_name` of students whose `student_id` is **in** (1, 3, 5).

### Resources:

- [SQL BETWEEN Operator](https://www.w3schools.com/sql/sql_between.asp)
- [SQL IN Operator](https://www.w3schools.com/sql/sql_in.asp)

### Expected Results:

**Part A Result:**

| first_name | last_name    |
|------------|--------------|
| Mustafa    | Sarvarov     |
| Arthur     | Kim          |
| Elnar      | Moldabekov   |

**Part B Result:**

| first_name | last_name    |
|------------|--------------|
| Mustafa    | Sarvarov     |
| Elnar      | Moldabekov   |
| Edmond     | Dantes       |

### Tip

- You can write several queries in one file

---
