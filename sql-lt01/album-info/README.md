# album-info

| Expected file |
| ------------- |
| `album-info.sql` |

Show information about albums and their artists.

Show:
- Album title as `AlbumTitle`
- Artist name as `Artist`
- Number of tracks as `TrackCount`
- Total price of all tracks as `TotalPrice`, rounded to 2 decimals

Note:
- Include only albums that have at least 5 tracks
- Sort the result by number of tracks in descending order

# Table: `artists`

```
| Column Name | Data Type   | Constraints          |
|-------------|-------------|----------------------|
| `ArtistId`  | INTEGER     | PRIMARY KEY, AUTOINCREMENT |
| `Name`      | NVARCHAR(120) | NULLABLE          |
```

# Table: `albums`

```
| Column Name | Data Type   | Constraints                           |
|-------------|-------------|---------------------------------------|
| `AlbumId`   | INTEGER     | PRIMARY KEY, AUTOINCREMENT           |
| `Title`     | NVARCHAR(160) | NOT NULL                          |
| `ArtistId`  | INTEGER     | NOT NULL, FOREIGN KEY REFERENCES `artists(ArtistId)` |
```

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