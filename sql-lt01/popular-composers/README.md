# popular-composers

| Expected file |
| ------------- |
| `popular-composers.sql` |

Find composers who have tracks in multiple genres.

Show:

- Composer name as `ComposerName`
- Number of their tracks as `TrackCount`
- Number of `unique` genres as `GenreCount`

Note:

- Skip `NULL` composers, so the composer `IS NOT NULL`
- Only show composers who have tracks in more than 1 genre
- Sort the result by number of genres descending order

# Table: `tracks`

```
| Column Name    | Data Type     | Constraints                           |
|----------------|---------------|---------------------------------------|
| `TrackId`      | INTEGER       | PRIMARY KEY, AUTOINCREMENT           |
| `Name`         | NVARCHAR(200) | NOT NULL                            |
| `AlbumId`      | INTEGER       | FOREIGN KEY REFERENCES `albums(AlbumId)` |
| `MediaTypeId`  | INTEGER       | NOT NULL, FOREIGN KEY REFERENCES `media_types(MediaTypeId)` |
| `GenreId`      | INTEGER       | FOREIGN KEY REFERENCES `genres(GenreId)` |
| `Composer`     | NVARCHAR(220) | NULLABLE                            |
| `Milliseconds` | INTEGER       | NOT NULL                            |
| `Bytes`        | INTEGER       | NULLABLE                            |
| `UnitPrice`    | NUMERIC(10,2) | NOT NULL                            |
```
