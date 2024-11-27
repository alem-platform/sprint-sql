# Rock Star

| Expected file |
| ------------- |
| `rock-star.sql` |

Time to give rock stars their own VIP table!

### Instructions:

Create a comprehensive `rock_stars` table that captures the essence of musical legends with the following specifications:

1. **Basic Identification**
   - `RockStarId`: Primary key, auto-increment
   - `StageName`: Text, required, unique, min 3 and max 50 characters 
   - `BandName`: Optional text field

2. **Career Metrics**
   - `YearsActive`: Integer with range constraint (from 1 to 70 inclusive), default value to 1
   - `GuitarBrandPreference`: Predefined guitar brand preference with max length of 50 and **must be** one from next list: (
            'Fender', 'Gibson', 'Ibanez', 'PRS',
            'Gretsch', 'ESP', 'Jackson', 'Other')

3. **Financial Tracking**
   - `MonthlyRoyalties`: Decimal for precise earnings 
     * 8 characters long 
     * 2 digits after decimal point
     * Non-negative values
     * Default value is zero

4. **Career Timestamps**
   - `CareerStartDate`: **Date** of first professional performance
     * Default value is current time

5. **Foreign Key Relationships**:
    - Link to `artists` table via `ArtistId`
    - Link to `genres` table via `GenreId`
    - Both should not be null

### Resources:
- [SQLite CREATE TABLE](https://www.sqlitetutorial.net/sqlite-create-table/)
- [SQLite Constraints](https://www.tutorialspoint.com/sqlite/sqlite_constraints.htm)
- [SQLite CHECK](https://www.sqlitetutorial.net/sqlite-check-constraint/)