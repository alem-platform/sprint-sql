# Math Magician

| Expected file |
| ------------- |
| `math-magician.sql` |

Perform mathematical operations in your queries. Let's add some magic by adjusting test scores.

### Instructions:

1. First, add a column `test_score` (*INTEGER*) to the `students` table.
2. Update each student's `test_score`:

  >  Mustafa: 90  
  >  Arthur: 85  
  >  Elnar: 88  
  >  Charlotte: 95  
  >  Edmond: 70  
  >  Mercedes: 75  
  >  Albert: 99

2. Select `first_name`, `last_name`, `test_score`, and a new column `adjusted_score` that adds 5 bonus points to `test_score`.

So, you have to write 3 seperate queries and submit them all in one file (don't forget about `;` sign at the end of each query)

### Resources:

- [SQLite Arithmetic Operators](https://www.sqlite.org/lang_expr.html#:~:text=show-,2.%20Operators%2C%20and%20Parse%2DAffecting%20Attributes,-SQLite%20understands%20these)
- [SQLite ALTER TABLE](https://www.sqlite.org/lang_altertable.html)
- [SQLite UPDATE](https://www.sqlite.org/lang_update.html)
