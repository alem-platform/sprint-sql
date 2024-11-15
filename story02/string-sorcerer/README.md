# String Sorcerer

| Expected file |
| ------------- |
| `string-sorcerer.sql` |

Master string manipulation functions.

### Instructions:

Using the `employees` table, create a query that shows:
1. Concatenated first_name and last_name with space as `full_name`
2. Email domain (everything after '@') as `email_domain`
3. Position in lowercase as `job_title`
4. First 3 characters of department_id concatenated with last 3 characters of employee_id as `employee_code`
5. First letter of first_name concatenated with full last_name as `short_name`

### Expected Result:

| full_name      | email_domain | job_title       | employee_code | short_name   |
|----------------|--------------|-----------------|---------------|--------------|
| John Smith     | company.com  | senior engineer | 001_001      | JSmith      |
| Maria Garcia   | company.com  | lead developer  | 002_002      | MGarcia     |
[... rest of employees ...]