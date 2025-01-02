# Text Pattern Pro

| Expected file |
| ------------- |
| `text-pattern-pro.sql` |

Enhance your ability to combine pattern matching with string operations and conditional logic.

### Instructions:

Using all tables, create a queries that:

1. Displays `department_display` as:
   - If `budget` is above 1,000,000, display `name` in uppercase and append ' - LARGE BUDGET'.
   - If `budget` is between 500,000 and 1,000,000, display `name` in proper case (first letter of the first word in uppercase) and append ' - Medium Budget'.
   - If `budget` is below 500,000, display `name` in lowercase and append ' - small budget'.
   - Sort the query by `department_display` in descending order.

2. Displays `employee_info` where each employee:
   - Have a `first_name` where the second letter is 'a' or 'e'.
   - Have a `position` that ends with 'Manager' or 'Analyst'.
   
   For these employees, format the output as:
   - `"LAST_NAME, FIRST_NAME - position"`, i.e. last and first names in upper case and position in lower case.
   - Sort the result by `employee_info` in ascending order.


3. Displays `product_summary` where:
   - `name` contains exactly two words.
   - `rating` is higher than the average rating of all products.
   - Format output as: `"Product: *NAME* | Price: *PRICE* | Rating: *RATING*"`
   - Sort the result by `product_summary` in descending order.

### Resources:

- [SQLite CASE Expression](https://www.sqlite.org/lang_expr.html#the_case_expression:~:text=only%20evaluated%20once.-,7.%20The%20CASE%20expression,-A%20CASE%20expression)
- [SQLite Pattern Matching](https://www.sqlitetutorial.net/sqlite-like/)
- [SQLite Aggregate Functions](https://www.sqlite.org/lang_aggfunc.html)
- [SQLite Subqueries](https://www.sqlitetutorial.net/sqlite-subquery/)
- [SQLite upper() function](https://www.sqlite.org/lang_corefunc.html#instr:~:text=(X%2C%200.0625).-,upper(X),lower%2Dcase%20ASCII%20characters%20are%20converted%20to%20their%20upper%2Dcase%20equivalent.,-zeroblob(N))
- [SQLite substr() function](https://www.sqlite.org/lang_corefunc.html#substr:~:text=substr(X%2CY%2CZ)%0Asubstr,an%20alias%20for%20%22substr()%22%20beginning%20with%20SQLite%20version%203.34.)
