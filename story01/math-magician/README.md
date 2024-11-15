# Math Magician

| Expected file |
| ------------- |
| `math-magician.sql` |

Perform mathematical operations in your queries. Let's add some magic by adjusting test scores.

### Instructions:

- First, add a column `test_score` (INT) to the `students` table.
- Update each student's `test_score`:

  > - Mustafa: 90  
  > - Arthur: 85  
  > - Elnar: 88  
  > - Charlotte: 95  
  > - Edmond: 70  
  > - Mercedes: 75  
  > - Albert: 99

- Select `first_name`, `last_name`, `test_score`, and a new column `adjusted_score` that adds 5 bonus points to `test_score`.

### Resources:

- [SQL Arithmetic Operators](https://www.w3schools.com/sql/sql_operators.asp)
- [SQL ALTER TABLE Statement](https://www.w3schools.com/sql/sql_alter.asp)
- [SQL UPDATE Statement](https://www.w3schools.com/sql/sql_update.asp)

### Expected Result:

| first_name | last_name    | test_score | adjusted_score |
|------------|--------------|------------|----------------|
| Mustafa    | Sarvarov     | 90         | 95             |
| Arthur     | Kim          | 85         | 90             |
| Elnar      | Moldabekov   | 88         | 93             |
| Charlotte  | Montgomery   | 95         | 100            |
| Edmond     | Dantes       | 70         | 75             |
| Mercedes   | Herrera      | 75         | 80             |
| Albert     | Einstein     | 99         | 104            |

---
