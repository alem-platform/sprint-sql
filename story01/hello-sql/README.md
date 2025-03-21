# Hello SQL

| Expected file       |
| ------------------- |
| `hello-sql.sql` |

Welcome to the SQL Sprint! 🎉

We will start from the basics and learn what SQL is and how to use it to manage and query databases.

### What is SQL?

SQL (Structured Query Language) is a standard language for accessing and manipulating relational databases.

---

## How to Get Started?

### For `story01`

For the `story01` of this sprint, you will work with an **empty database**. You will create tables, insert data, and perform basic queries.

**Instructions:**

1. **Setting Up Your Environment:**

   - You will be working with **SQLite**, a lightweight, file-based database that's easy to use.

2. **Create a New SQLite Database:**

   - Open your terminal.
   - Navigate to the directory where you want to store your database files.
   - Create a new SQLite database file named `story01.db`:

     ```sh
     sqlite3 story01.db
     ```

   - This command opens the SQLite prompt connected to your new database.

   > Quick tip: enter `.help` to list all available commands (for example, `.exit` - is to exit the database prompt)

3. **Begin Working on Tasks:**

   - Follow the instructions in each task to create tables, insert data, and write queries.
   - You can execute your SQL scripts using the SQLite command line:

     ```sh
     sqlite3 story01.db < your_task_file.sql
     ```

---

### For `story02` and Beyond

Starting with `story02`, you will work with **prefilled databases** that contain data already populated. This will allow you to practice more advanced queries and operations.

**Instructions:**

1. **Accessing the Prefilled Databases:**

   - The prefilled SQLite database files for each story are available **[here](https://github.com/alem-platform/sprint-sql/blob/master/assets)**

2. **Download the Database Files:**

   - Navigate to the specific database file you need (e.g., `week01.db`).
   - Click on the file and then click the **Download** button to save it to your local machine.
   - Save the database file in the directory where you will be working on your SQL tasks.

3. **Begin Working on Tasks:**

   - Use the downloaded database file to execute your queries.
   - You can interact with the database using the SQLite command line:

     ```sh
     sqlite3 week01.db
     ```

   - To execute your SQL scripts against the database:

     ```sh
     sqlite3 week01.db < your_task_file.sql
     ```

4. **Do Not Modify the Database Structure:**

   - Unless a task explicitly instructs you to do so, do not alter the schema of the prefilled databases.
   - Focus on writing queries and operations that work with the existing data.

---

   ## Your first task

   Let's create your first SQL program 

   - Create a sql file named `hello-sql.sql `

   ```sh
   echo 'SELECT "Hello SQL!";' > hello-sql.sql
   ```

   - Test your query

   ```sh
   sqlite3 welcome.db < hello-sql.sql
   ```

   - You should see the message on your console

   ```sh
   Hello SQL!
   ```

   ## Working in Your Repository

   For this bootcamp, you will work in the `sprint-sql` repository, create it and add your `hello-sql.sql` into it. This repository will store all your sprint solutions.

---

## Important Notes:

- **Consistency is Key:**

  - Use the exact database files provided to ensure your queries work correctly.
  - Do not modify the data in the prefilled databases unless a task explicitly requires it.
  - If you did modify it accidentaly or whatever reason you had, you can always redownload the database and use the new one

---

## Resources

- [SQL Wikipedia](https://ru.wikipedia.org/wiki/SQL)
- [SQLite Documentation](https://sqlite.org/docs.html)
- [Prefilled Databases](https://github.com/alem-platform/sprint-sql/blob/master/assets)

