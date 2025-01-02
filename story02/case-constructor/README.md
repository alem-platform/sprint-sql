# Case Constructor

| Expected file |
| ------------- |
| `case-constructor.sql` |

Learn to apply conditional logic using `CASE` expressions.

### Instructions:

Using the `employees` table, create a query showing:
1. `full_name` which consists of `first_name` and `last_name` separated by single space
2. `salary_category` based on `salary`:
   - Above 75,000: **'High'**
   - 50,000–75,000: **'Medium'**
   - Below 50,000: **'Low'**
3. `employee_type` based on `department_id`:
   - Department 1–5: **'Core Team'**
   - Department 6–10: **'Support Team'**

Sort the query by `full_name` in descending order.

### Resources:

- [SQLite CASE Expression](https://www.sqlite.org/lang_expr.html#the_case_expression:~:text=only%20evaluated%20once.-,7.%20The%20CASE%20expression,-A%20CASE%20expression)
