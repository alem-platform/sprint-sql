# Maximum Safety

| Expected file |
| ------------- |
| `maximum-safety.sql` |

Write complex transaction with maximum safety

### Instructions:

Write a transaction that:
1. Creates a new record label (insert into artists) called "Acquired Records"
2. Transfers all artists that have less than 2 albums to this new label 
   (update their albums to be under the new artist)
3. Updates all transferred tracks to have a 20% discount on their price
4. Deletes the original artists that were transferred

### Resources:
- [SQLite Transactions](https://www.sqlite.org/lang_transaction.html)
- [SQLite Subqueries](https://www.w3resource.com/sqlite/sqlite-subqueries.php)
- [SQLite Join](https://www.sqlitetutorial.net/sqlite-join/)