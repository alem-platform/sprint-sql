# Text Pattern Pro

| Expected file |
| ------------- |
| `text-pattern-pro.sql` |

Enhance your ability to combine pattern matching with string operations and conditional logic.

### Instructions:

Using the `employees`, `departments`, and `products` tables, create a queries that:

1. Displays `department_display` as:
   - If `budget` is above 1,000,000, display `name` in uppercase and append ' - LARGE BUDGET'.
   - If `budget` is between 500,000 and 1,000,000, display `name` in proper case (first letter uppercase) and append ' - Medium Budget'.
   - If `budget` is below 500,000, display `name` in lowercase and append ' - small budget'.

2. Displays `employee_info` where each empolyee:
   - Have a `first_name` where the second letter is 'a' or 'e'.
   - Have a `position` that ends with 'Manager' or 'Director'.
   
   For these employees, format the output as:
   - `employee_info`: "<LAST_NAME, first_name> - POSITION in DEPARTMENT_NAME"

3. Displays `product_summary` where:
   - `name` contains exactly two words.
   - `rating` is higher than the average rating of all products.
   - Format `product_summary` as: "Product: *NAME* | Price: *PRICE* | Rating: *RATING*"

### Resources:

- [SQL CASE Statement](https://www.w3schools.com/sql/sql_case.asp)
- [SQLite String Operations](https://www.sqlitetutorial.net/sqlite-string-functions/)
- [SQLite Pattern Matching](https://www.sqlitetutorial.net/sqlite-like/)
- [SQLite Aggregate Functions](https://www.sqlite.org/lang_aggfunc.html)

---