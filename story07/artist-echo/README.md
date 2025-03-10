# Artist Echo

| Expected file |
| ------------- |
| `artist-echo.sql` |

Marketing team needs data about our artists' performance. 

## Instructions:

Create a query showing:

- Artist name as it is
- Total number of **unique** tracks they have as `TrackCount`
- Number of **unique** albums as `AlbumCount`
- Number of **unique** playlists featuring their tracks as `PlaylistCount`
- Total revenue from all their tracks as `TotalRevenue`
- Average track price as `AverageTrackPrice`
- Their best selling track name as `TopTrack`

Note:
- Include artists' **all** tracks
- Round all money values to 2 decimal places
- Only include artists who have at least one unique track
- Order by total revenue descending
- Limit to top 50 artists

## Resources:

- [SQLite Subqueries](https://www.w3resource.com/sqlite/sqlite-subqueries.php)
- [SQLite Aggregate Functions](https://www.sqlite.org/lang_aggfunc.html)
- [SQLite JOIN](https://www.sqlitetutorial.net/sqlite-join/)
- [SQLite HAVING](https://www.sqlitetutorial.net/sqlite-having/)
- [SQLite ROUND Function](https://www.sqlite.org/lang_corefunc.html#round)
- [SQLite LEFT JOIN](https://www.sqlite.org/lang_select.html#joins)
