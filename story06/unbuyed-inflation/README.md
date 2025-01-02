# Unbuyed Inflation

| Expected file |
| ------------- |
| `unbuyed-inflation.sql` |

Let's apply inflation on tracks that haven't been purchased yet (is it smart move to do?)

## Instructions:

Write an UPDATE statement that:
- Increases the UnitPrice by 10% for all tracks longer than 6 minutes
- Only applies to tracks that haven't been purchased yet (not in `invoice_items`)

## Resources:

- [SQLite UPDATE](https://sqlite.org/lang_update.html)
- [SQLite Subqueries](https://www.w3resource.com/sqlite/sqlite-subqueries.php)