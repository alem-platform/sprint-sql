# composer-tracks

| Expected file |
| ------------- |
| `composer-tracks.sql` |

Find composers who wrote more than `10` tracks.

Show:

- Composer's name as it is
- Number of their tracks as `TrackCount`

Note:

- Skip composers that are `NULL`, so the composer `IS NOT NULL`
- Only show composers with more than 10 tracks
- Sort the result by number of tracks in descending order

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