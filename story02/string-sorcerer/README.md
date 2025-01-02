# String Sorcerer

| Expected file |
| ------------- |
| `string-sorcerer.sql` |

Master basic string manipulation functions.

### Instructions:

Using the `employees` table, create a query that shows:
1. Concatenated `first_name` and `last_name` with a space as `full_name`.
2. The email domain (everything after `'@'`) as `email_domain`.
3. Position in uppercase as `job_title`.

Sort the query by `full_name` in ascending order.

### Resources:

- [SQLite substr() function](https://www.sqlite.org/lang_corefunc.html#substr:~:text=substr(X%2CY%2CZ)%0Asubstr,an%20alias%20for%20%22substr()%22%20beginning%20with%20SQLite%20version%203.34.)
- [SQLite instr() function](https://www.sqlite.org/lang_corefunc.html#instr:~:text=ELSE%20Z%20END%22.-,instr(X%2CY),are%20NULL%20in%20instr(X%2CY)%20then%20the%20result%20is%20NULL.,-last_insert_rowid())
- [SQLite upper() function](https://www.sqlite.org/lang_corefunc.html#instr:~:text=(X%2C%200.0625).-,upper(X),lower%2Dcase%20ASCII%20characters%20are%20converted%20to%20their%20upper%2Dcase%20equivalent.,-zeroblob(N))
