## Core Functionality

### Has the team created an accurate Entity-Relationship Diagram (ERD) representing at least five entities?

- [ ] Yes
- [ ] No

### Are the entities in the ERD clearly defined with appropriate attributes (minimum of five attributes per entity)?

- [ ] Yes
- [ ] No

### Does the ERD show logical relationships between entities?

- [ ] Yes
- [ ] No

### Have all required tables been created according to the ERD?

- [ ] Yes
- [ ] No

### Are the tables created with appropriate data types and constraints (e.g., `PRIMARY KEY`, `NOT NULL`)?

- [ ] Yes
- [ ] No

### Are at least 10 records inserted into each table with realistic and consistent data?

- [ ] Yes
- [ ] No

### Do the data entries maintain logical consistency between related entities (e.g., `book_id` in `Loans` exists in `Books`)?

- [ ] Yes
- [ ] No

### Has the team provided SQL scripts for table creation and data insertion (`create_tables.sql` and `insert_data.sql`)?

- [ ] Yes
- [ ] No

### Do the SQL queries correctly perform all the required tasks specified in the instructions?

- [ ] Yes
- [ ] No

## Data Retrieval and Analysis

### 1. Does the team correctly perform basic `SELECT` queries on the `Books` table (retrieve all columns)?

- [ ] Yes
- [ ] No

### 2. Can the team retrieve specific columns (`title`, `year_published`) from the `Books` table?

- [ ] Yes
- [ ] No

### 3. Has the team successfully added a new patron to the `Patrons` table?

- [ ] Yes
- [ ] No

### 4. Are column operations and aliases used correctly (e.g., concatenating `first_name` and `last_name` as `full_name`)?

- [ ] Yes
- [ ] No

### 5. Does the team list books with a calculated column showing the age of the book?

- [ ] Yes
- [ ] No

### 6. Can the team filter data to find books published after the year 2000?

- [ ] Yes
- [ ] No

### 7. Has the team listed all patrons with the last name 'Smith'?

- [ ] Yes
- [ ] No

### 8. Are pattern matching and sorting operations performed correctly (e.g., finding books with titles starting with 'The')?

- [ ] Yes
- [ ] No

### 9. Does the team sort the list of books by `year_published` in descending order?

- [ ] Yes
- [ ] No

### 10. Are text operations applied correctly (e.g., displaying patron emails in uppercase)?

- [ ] Yes
- [ ] No

### 11. Has the team used aggregate functions to calculate the total number of books?

- [ ] Yes
- [ ] No

### 12. Can the team find the oldest book in the library using aggregate functions?

- [ ] Yes
- [ ] No

### 13. Are grouping operations used to count the number of books per author?

- [ ] Yes
- [ ] No

### 14. Has the team applied filtering groups to list authors who have written more than 2 books?

- [ ] Yes
- [ ] No

### 15. Does the team use single value subqueries to find the book(s) with the highest number of loans?

- [ ] Yes
- [ ] No

### 16. Has the team used correlated subqueries to find patrons who have borrowed **every book** in the 'Science Fiction' genre?

- [ ] Yes
- [ ] No

### 17. Did the team display each author's name and the **average age** of their books?

- [ ] Yes
- [ ] No

### 18. Has the team found all books that have **never been borrowed** and were published **before the average publication year** of all books?

- [ ] Yes
- [ ] No

### 19. Did the team display each patron's name and the **total number of books borrowed**, including only books published after 2010?

- [ ] Yes
- [ ] No

### 20. Has the team listed all books along with the **number of times each has been borrowed** using a subquery in the `SELECT` clause?

- [ ] Yes
- [ ] No

### 21. Did the team find all authors whose last name contains 'son' and who have written at least one book with 'Data' in the title?

- [ ] Yes
- [ ] No

### 22. Has the team identified all loans that are **overdue by more than 30 days** using date calculations?

- [ ] Yes
- [ ] No

### 23. Did the team find the genre with the **highest average book age** using combined aggregate functions?

- [ ] Yes
- [ ] No

### 24. Has the team listed all patrons who have borrowed **more books than the average number of books borrowed** by all patrons?

- [ ] Yes
- [ ] No

## Edge Case Handling

### Does the database handle cases where a book has no loans (e.g., books never borrowed)?

- [ ] Yes
- [ ] No

### Are queries able to handle cases with zero results (e.g., authors with no books)?

- [ ] Yes
- [ ] No

### Does the team ensure data integrity by maintaining consistent relationships between tables?

- [ ] Yes
- [ ] No

### Is there error handling for data insertion anomalies (e.g., inserting a loan with a non-existent `book_id` or `patron_id`)?

- [ ] Yes
- [ ] No

## Code Quality

### Are SQL scripts well-organized and easy to follow?

- [ ] Yes
- [ ] No

### Are clear and descriptive comments used throughout the SQL scripts, indicating which task each query corresponds to?

- [ ] Yes
- [ ] No

### Do table and column names follow consistent and meaningful naming conventions?

- [ ] Yes
- [ ] No

### Is the SQL code formatted consistently (e.g., proper indentation, capitalization of SQL keywords)?

- [ ] Yes
- [ ] No

### Are complex queries broken down and documented appropriately for clarity?

- [ ] Yes
- [ ] No

## Usability

### Has the team provided clear instructions for setting up the database?

- [ ] Yes
- [ ] No

### Are descriptions of each query and its purpose included in the `queries.sql` file?

- [ ] Yes
- [ ] No

### Does the database handle invalid data gracefully (e.g., appropriate error messages, constraints preventing bad data)?

- [ ] Yes
- [ ] No

### Are results from queries neatly formatted and easy to read in the `results.txt` document?

- [ ] Yes
- [ ] No

## Bonus Features

### Advanced Subqueries

#### Has the team implemented correlated subqueries for complex data retrieval?

- [ ] Yes
- [ ] No

#### Example: Did they find patrons who have borrowed **all books by a particular author**?

- [ ] Yes
- [ ] No

### Data Constraints

#### Has the team implemented additional constraints like `UNIQUE`, `CHECK`, or `DEFAULT`?

- [ ] Yes
- [ ] No

#### Do these constraints enhance data integrity effectively?

- [ ] Yes
- [ ] No

### Indexing

#### Has the team created indexes on frequently queried columns to improve performance?

- [ ] Yes
- [ ] No

#### Is there evidence of improved query performance due to indexing (e.g., query execution time comparisons)?

- [ ] Yes
- [ ] No

## Project Presentation and Code Defense

### Can the team clearly explain their database design and the relationships between entities?

- [ ] Yes
- [ ] No

### Are they able to effectively answer questions about their SQL queries and the logic behind them?

- [ ] Yes
- [ ] No

## Detailed Feedback

### What was great? What did you like the most about the project and the team's performance?

### What could be better? How could these improvements positively impact the outcome?
