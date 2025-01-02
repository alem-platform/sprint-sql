# Join Yourself

| Expected file |
| ------------- |
| `join-yourself.sql` |

Did you know that you can **join yourself**? 

## Instructions:

Write a query that retrieves:

1. Each **manager's** `FirstName`, `LastName`, and `Title`.
2. The total number of subordinates assigned to each manager (`SubordinateCount`).
3. Exclude managers who do not have any subordinates.

> Sort the output by `ManagerLastName` and `ManagerFirstName` in ascending order.

## Expected Output Columns:
- `ManagerFirstName`: The first name of the manager.
- `ManagerLastName`: The last name of the manager.
- `ManagerTitle`: The title of the manager.
- `SubordinateCount`: The number of subordinates reporting to the manager.

**Managers are the ones to whom employees report**

## Resources:

- [SQLite Self Join](https://www.sqlitetutorial.net/sqlite-self-join/)
- [SQLite Aggregate Functions](https://www.sqlite.org/lang_aggfunc.html)
