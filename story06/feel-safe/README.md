# Feel Safe

| Expected file |
| ------------- |
| `feel-safe.sql` |

Practice using transactions with different types of operations, feel safe to make mistakes

### Instructions:

Write a transaction that:
1. Starts a new transaction
2. Inserts a new genre **"Podcast"**
3. Deletes all playlists that have no tracks (not present in playlist_track table)
4. Inserts a new album **"Witcher"** with `ArtistId` - 7
5. Commits if all operations succeed

**Important!**

1. First, try to test transaction locally and use next insertion instead of the one required in the task:
```
    INSERT INTO albums (title, artistid)
    VALUES ('Witcher', null);
```
2. Transaction will give you an error
3. **ROLLBACK**, fix the insertion query and try again to run the transaction

### Resources:
- [SQLite Transactions](https://www.sqlite.org/lang_transaction.html)
- [SQLite DELETE](https://www.sqlite.org/lang_delete.html)
- [SQLite INSERT](https://www.sqlite.org/lang_insert.html)
- [ACID Properties](https://www.geeksforgeeks.org/acid-properties-in-dbms/)