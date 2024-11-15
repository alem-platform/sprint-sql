# Text Pattern Pro

| Expected file |
| ------------- |
| `text-pattern-pro.sql` |

Combine pattern matching with string operations.

### Instructions:

Using all tables, create a query that:
1. Shows department name in uppercase if budget > 800000, otherwise in lowercase
2. Lists all employees where:
   - First name contains 'a' or 'e'
   - Last name is longer than 6 characters
   - Position contains either 'Senior' or 'Lead'
3. Format the output as: "NAME (POSITION) - DEPARTMENT"

### Expected Result:

| employee_info                                  | department_display |
|-----------------------------------------------|-------------------|
| Maria Garcia (Lead Developer) - Development    | development      |
| James Wilson (Senior Engineer) - ENGINEERING   | ENGINEERING      |
[... matching employees ...]