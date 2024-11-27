# Table Morph

| Expected file |
| ------------- |
| `table-morph.sql` |

*Tranform yourself, tarnished table... **Epoximise!***

### Instructions:

- Add a new column `DownloadCount` that should be whole integer number, is required, default value is *0*
- Add a new column `LastPlayedDate` that would show date and **time** of last played track, is optional, *no default value*
- Add a column `IsExplicit` that is boolean that shows that track is expiclit or not, is required, default value is *true*

### Tip


```sql
PRAGMA table_info(asdf)
```

### Resources:

- [SQLite ALTER TABLE](https://www.sqlite.org/lang_altertable.html)
- [SQLite Column Constraints](https://www.tutorialspoint.com/sqlite/sqlite_constraints.htm)
- [SQLite Data Types](https://www.sqlite.org/datatype3.html)