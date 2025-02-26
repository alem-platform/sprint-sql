# playlist-genres

| Expected file |
| ------------- |
| `playlist-genres.sql` |

Show which genres are in each playlist.

Show:
- Playlist name as `Playlist`
- Genre name as `Genre`
- Number of tracks as `TrackCount`

Note:
- Show all playlists **even** if they have no tracks
- Group the result by id of the playlist and it's name
- Sort the result by playlist name in ascending order, then by number of tracks in descending order

# Table: `genres`

```
| Column Name | Data Type     | Constraints          |
|-------------|---------------|----------------------|
| `GenreId`   | INTEGER       | PRIMARY KEY, AUTOINCREMENT |
| `Name`      | NVARCHAR(120) | NULLABLE            |
```

# Table: `playlists`

```
| Column Name  | Data Type     | Constraints          |
|--------------|---------------|----------------------|
| `PlaylistId` | INTEGER       | PRIMARY KEY, AUTOINCREMENT |
| `Name`       | NVARCHAR(120) | NULLABLE            |
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

# Table: `playlist_track`

```
| Column Name  | Data Type     | Constraints                                |
|--------------|---------------|--------------------------------------------|
| `PlaylistId` | INTEGER       | NOT NULL, FOREIGN KEY REFERENCES `playlists(PlaylistId)` |
| `TrackId`    | INTEGER       | NOT NULL, FOREIGN KEY REFERENCES `tracks(TrackId)` |
```
