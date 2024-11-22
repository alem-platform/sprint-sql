# crunch01: Library Management System

Greetings team. As part of our initiative to modernize our library's systems, we have an important project that requires your expertise. You are being assigned to develop a comprehensive **Library Management System** to digitize our catalog and streamline borrowing activities. This project simulates a real-world scenario where teamwork and collaboration are essential.

Your task is to work together to design and implement a database system that meets the needs of our library. Effective communication and division of responsibilities will be key to your success.

Remember, challenges may arise, but they are opportunities for growth. Embrace them, support each other, and strive to deliver a robust solution.

Good luck. This project is a significant milestone. Learn from it, and let it propel you forward.

### Project Brief

You are tasked with creating a **Library Management System** for a local library. The library wants to digitize its catalog and keep track of books, patrons, and borrowing activities.

### Objectives

- Design and create a database schema suitable for a library system.
- Develop an Entity-Relationship Diagram (ERD) to plan your database structure.
- Implement the database using SQL, focusing on creating tables and inserting data.
- Write SQL queries to perform data retrieval and analysis.
- Apply SQL concepts from basic table operations to nested queries.

## Instructions

### Database Design

- **Create an Entity-Relationship Diagram (ERD):**
  - **Purpose:** To visually represent the database structure and the relationships between different entities.
  - **Requirements:**
    - Identify at least **five** entities relevant to a library system. Examples include `Books`, `Patrons`, `Loans`, `Authors`, `Genres`.
    - Define attributes for each entity (minimum of five attributes per entity).
    - Determine primary keys for each entity.
    - Even though you haven't learned about foreign keys yet, think about how the entities are related and how you might represent those relationships.
  - **Deliverable:** A clear ERD diagram. You can use tools like [draw.io](https://app.diagrams.net/) or hand-draw it and scan it.

- **Resources:**
  - [Introduction to ER Diagrams](https://www.lucidchart.com/pages/er-diagrams)
  - [How to Create an ER Diagram](https://www.smartdraw.com/entity-relationship-diagram/)

### Table Creation

- **Implement the Database Schema:**
  - **Create Tables:**
    - Use your ERD to create SQL `CREATE TABLE` statements for each entity.
    - Define appropriate data types for each attribute.
    - Implement basic constraints like `PRIMARY KEY` and `NOT NULL`.
    - Since you haven't covered foreign keys yet, you don't need to include them.
  - **Entities Examples:**
    - `Books` (e.g., `book_id`, `title`, `author_id`, `genre_id`, `year_published`)
    - `Patrons` (e.g., `patron_id`, `first_name`, `last_name`, `email`, `phone_number`)
    - `Loans` (e.g., `loan_id`, `book_id`, `patron_id`, `loan_date`, `return_date`)
    - `Authors` (e.g., `author_id`, `first_name`, `last_name`, `birth_year`)
    - `Genres` (e.g., `genre_id`, `name`, `description`)

- **Deliverable:** SQL script (`create_tables.sql`) with all `CREATE TABLE` statements.

### Data Insertion

- **Populate the Tables:**
  - Insert at least **10 records** into each table.
  - Ensure that the data is realistic and that relationships between entities are logically consistent.
    - For example, when inserting data into `Loans`, make sure the `book_id` and `patron_id` exist in the `Books` and `Patrons` tables, respectively.
  - Even though you're not using foreign keys, maintain data consistency manually.

- **Deliverable:** SQL script (`insert_data.sql`) with all `INSERT INTO` statements.

### Data Retrieval and Analysis

Based on the topics covered in **Week 1**, perform the following tasks:

1. **Basic SELECT Queries:**
   - Retrieve all columns from the `Books` table.
   - Select specific columns (`title`, `year_published`) from the `Books` table.

2. **Simple Data Entries:**
   - Add a new patron to the `Patrons` table.

3. **Column Operations and Aliases:**
   - Retrieve the full name of patrons by concatenating `first_name` and `last_name` as `full_name`.
   - List all books with a calculated column showing the age of the book (`current_year - year_published`) as `book_age`.

4. **Filtering Data:**
   - Find all books published after the year 2000.
   - List all patrons with the last name 'Smith'.

5. **Pattern Matching and Sorting:**
   - Find all books with titles starting with 'The'.
   - Sort the list of books by `year_published` in descending order.

6. **Text Operations:**
   - Display all patron emails in uppercase.
   - Find all patrons whose first name ends with 'a'.

7. **Unique Values:**
   - List all unique genres available in the `Books` table.

8. **Aggregate Functions:**
   - Calculate the total number of books in the library.
   - Find the oldest book in the library (minimum `year_published`).

9. **Grouping Operations:**
   - Count the number of books per author.
   - Find the average number of books loaned per patron.

10. **Filtering Groups:**
    - List authors who have written more than 2 books.
    - Find patrons who have borrowed more than 3 books.

11. **Single Value Subqueries:**
    - Find the book(s) with the highest number of loans.

12. **Correlated Subqueries:**
    - **Task:** Find all patrons who have borrowed **every book** in the 'Science Fiction' genre.

13. **Nested Aggregates:**
    - **Task:** For each author, display their name and the **average age** of their books.

14. **Complex Filtering:**
    - **Task:** Find all books that have **never been borrowed** and were published **before the average publication year** of all books.

15. **Conditional Aggregation:**
    - **Task:** For each patron, display their name and the **total number of books borrowed**, but only include books published after 2010.

16. **Subqueries in SELECT Clause:**
    - **Task:** List all books along with the **number of times each has been borrowed**.

17. **Advanced Pattern Matching:**
    - **Task:** Find all authors whose last name contains the letter sequence 'son' and who have written at least one book with 'Data' in the title.

18. **Date Calculations:**
    - **Task:** Identify all loans that are **overdue by more than 30 days**.

19. **Combined Aggregate Functions:**
    - **Task:** Find the genre with the **highest average book age**.

20. **Nested Subqueries and Aggregation:**
    - **Task:** List all patrons who have borrowed **more books than the average number of books borrowed** by all patrons.

## Bonus Tasks

### 1. Advanced Subqueries

**Correlated Subqueries:**

- Use correlated subqueries for more complex data retrieval.
- *Example:* Find patrons who have borrowed all books by a particular author.

### 2. Data Constraints

**Additional Constraints:**

- Implement constraints such as `UNIQUE`, `CHECK`, or `DEFAULT` to enhance data integrity.

### 3. Indexing

**Performance Optimization:**

- Create indexes on columns frequently used in `WHERE` clauses to improve query performance.

## Submission

### ERD

- Submit your ERD as an image file.

### SQL Scripts

- `create_tables.sql` with your table creation statements
- `insert_data.sql` with your data insertion statements
- `queries.sql` containing all your SQL queries for the tasks above
  - Include comments to indicate which task each query corresponds to

### Query Results

- Provide a document (`results.txt`) containing the output results of your queries
- Ensure results are well-formatted and readable

## Assessment Criteria

Here's what your reviewers will be looking at:

### **Functionality**

#### Database Design

- The ERD accurately represents entities and their relationships.
- The database schema correctly implements the designed ERD.
- Tables are created with appropriate data types and constraints.

#### Data Population

- Tables are populated with realistic and consistent data.
- Relationships between entities are logically maintained.

#### SQL Queries

- Queries correctly perform the required tasks.
- Appropriate use of SQL syntax and functions.
- Queries handle edge cases such as zero results or duplicates.

### **Code Quality**

#### Readability

- SQL scripts are well-organized and easy to follow.
- Clear and descriptive comments and naming conventions are used.

#### Efficiency

- Queries are optimized and avoid unnecessary computations.

#### Modularity

- Code is modular with distinct sections for different tasks.
- Avoids code duplication and promotes reusability.

### **Usability**

#### Documentation

- Clear instructions for setting up the database.
- Descriptions of each query and its purpose.

#### Error Handling

- Ensures data integrity through constraints and validations.

#### Presentation

- Results are neatly formatted and easy to read.
- Output aligns with the expected results.

### Bonus Tasks

#### **Correlated Subqueries**

##### Implementation

- Correctly implements correlated subqueries to perform complex data retrieval.
- The queries accurately reflect scenarios such as finding patrons who have borrowed all books by a particular author.

##### Functionality

- Demonstrates understanding of correlated subqueries by using them appropriately within the SQL statements.
- Ensures queries return correct and expected results.

##### Code Quality

- Queries are well-documented with comments explaining the logic.
- Maintains readability and follows SQL best practices.

#### **Additional Constraints**

##### Implementation

- Successfully implements additional constraints like `UNIQUE`, `CHECK`, or `DEFAULT` in the table definitions.
- Constraints enhance data integrity and prevent invalid data entries.

##### Functionality

- Validates that constraints are enforced by attempting to insert invalid data and checking for appropriate error messages.
- Ensures that data integrity is maintained throughout database operations.

##### Documentation

- Properly documents the constraints and explains their purpose in maintaining database integrity.

#### **Performance Optimization**

##### Implementation

- Creates indexes on columns that are frequently used in `WHERE` clauses or join conditions.
- Indexes are appropriately chosen to enhance query performance without unnecessary overhead.

##### Functionality

- Demonstrates improved query performance due to indexing.
- Provides analysis or evidence of performance enhancement, such as query execution time comparisons before and after indexing.

##### Code Quality

- Index creation scripts are well-organized and documented.
- Avoids over-indexing which can degrade performance.

## Resources

- [SQLite Documentation](https://www.sqlite.org/docs.html)
- [SQL Tutorial](https://www.w3schools.com/sql/)
- [Introduction to ER Diagrams](https://www.lucidchart.com/pages/er-diagrams)
- [How to Create an ER Diagram](https://www.smartdraw.com/entity-relationship-diagram/)
- [SQL Constraints](https://www.w3schools.com/sql/sql_constraints.asp)
- [SQL Aggregate Functions](https://www.sqltutorial.org/sql-aggregate-functions/)
- [SQLite Data Types](https://www.sqlite.org/datatype3.html)
- [SQL Correlated Subqueries](https://www.w3schools.com/sql/sql_subqueries.asp)
