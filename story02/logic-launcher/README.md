# Logic Launcher

| Expected file |
| ------------- |
| `logic-launcher.sql` |

Apply logical operators to create complex conditions.

### Instructions:

Using the `employees` and `departments` tables, create queries to find, **WITHOUT** using `JOIN`:
1. Engineers (any position containing `'Engineer'`) with salary > 50000 
2. Employees in `Human Resources` OR `Finance` departments
3. Employees NOT in `Logistics` department who make more than 50000
4. Analysts hired in between `2012-01-01` and `2016-12-31` with salary less than `70000`

In all queries, select the employee's first name, last name, position, salary, departamnt id and hire date *AS* they are *AND* sort them by first name in descending order

### Resources:

- [SQLite Subqueries](https://www.sqlitetutorial.net/sqlite-subquery/)
- [SQLite IN Operator](https://www.sqlitetutorial.net/sqlite-in/)
- [SQLite NOT Operator](https://www.techonthenet.com/sqlite/not.php)
- [SQLite LIKE Operator](https://www.sqlitetutorial.net/sqlite-like/)
- [SQLite BETWEEN Operator](https://www.sqlitetutorial.net/sqlite-between/)
