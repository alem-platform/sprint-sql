# DML Zone

**You are entering a DML(Data Manipulation Language) Zone**

This story consists of task that requires database change, but each task is isolated from each other, this means that results of one task would not be saved and used in other tasks.

> Little tip from me - redownload database for each task to minize the risk of human factor when testing your queries.

---

# External Insert

| Expected file |
| ------------- |
| `external-insert.sql` |

Let's invade the classical music genre with some rock!

### Instructions:

Insert all **Rock** genre tracks (use a subquery to find the genre_id for 'Rock') that are longer than 5 minutes into the **'Classical'** playlist (use a subquery to find the playlist_id).

### Resources:

- [SQLite Insert with Select](https://www.sqlitetutorial.net/sqlite-insert/)
- [SQL Subqueries](https://www.w3resource.com/sqlite/sqlite-subqueries.php)
