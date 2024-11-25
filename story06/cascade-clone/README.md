# Cascade Clone

| Expected file |
| ------------- |
| `cascade-clone.sql` |

Mimic the `CASCADE` behaviour and remove a specific media type and all related data from the database.

### Instructions:

Write a queries that:
- Remove all related from playlist_track and invoice_items
- Removes all tracks of 'MPEG audio file' media type
- Finally remove the media type itself

**Handle deletions in correct order to maintain referential integrity**

### Resources:
- [SQLite DELETE](https://www.sqlitetutorial.net/sqlite-delete/)
- [SQLite Casacde](https://www.scaler.com/topics/sql/cascade-in-sql/)