# Case Constructor

| Expected file |
| ------------- |
| `case-constructor.sql` |

Master CASE expressions for conditional text handling.

### Instructions:

Create a query using `employees` and `departments` tables showing:
1. `full_name` (first_name + ' ' + last_name)
2. Salary category:
   - Above 5500: 'High'
   - 4500-5500: 'Medium'
   - Below 4500: 'Entry'
3. Experience level based on hire_date:
   - Before 2022: 'Veteran'
   - 2022: 'Intermediate'
   - 2023 and after: 'Novice'
4. Department size based on budget:
   - Above 800000: 'Large'
   - 500000-800000: 'Medium'
   - Below 500000: 'Small'

### Expected Result:

| full_name      | salary_category | experience_level | department_size |
|----------------|-----------------|------------------|-----------------|
| John Smith     | Medium          | Veteran          | Large          |
| Maria Garcia   | High            | Veteran          | Medium         |
| Michael Brown  | Medium          | Intermediate     | Large          |
[... rest of employees ...]