# Welcome

| Expected file    |
| ---------------- |
| `welcome.sql`    |

Welcome to the SQL Sprint! 🎉

We will start from the basics and learn what SQL is and how to use it to manage and query databases.

### What is SQL?

SQL (Structured Query Language) is a standard language for accessing and manipulating relational databases.

### How to Get Started?

#### For story01

For the first part of this sprint, you will work with an **empty database**. You will create tables, insert data, and perform basic queries.

**Instructions:**

1. **Setting Up Your Environment:**

    - You will be working with SQLite, a lightweight, file-based database that's easy to use and already installed on your machines.

2. **Create a New SQLite Database:**

    - Open your terminal.
    - Navigate to the directory where you want to store your database files.
    - Create a new SQLite database file named `story01.db`:

      ```sh
      sqlite3 story01.db
      ```

    - This command opens the SQLite prompt connected to your new database.

3. **Begin Working on Tasks:**

    - Follow the instructions in each task to create tables, insert data, and write queries.
    - You can execute your SQL scripts using the SQLite command line:

      ```sh
      sqlite3 story01.db < your_task_file.sql
      ```

#### For story02 and so on

Starting with `story02` and so on, you will work with a **prefilled database** that contains data already populated. This will allow you to practice more advanced queries and operations.

We have prepared a Docker image that contains the SQLite database with the prefilled data.

**Instructions:**

1. **Download the Docker Image:**

    - Download the Docker image from the provided link:

      [Download Docker Image](http://example.com/sql_sprint_image.tar)

      *(Replace with the actual link provided by your instructor.)*

2. **Load the Docker Image:**

    - Open your terminal or command prompt.
    - Load the Docker image into your local Docker registry:

      ```sh
      docker load -i sql_sprint_image.tar
      ```

    - This command will import the image and make it available for you to use.

3. **Run the Docker Container:**

    - Start a container from the image:

      ```sh
      docker run -d --name sql_sprint_container sql_sprint_image
      ```

    - This command runs the container in detached mode.

4. **Accessing the SQLite Database Inside the Container:**

    - To interact with the SQLite database inside the container, you can execute commands within the container's shell.

    - Start a shell session inside the running container:

      ```sh
      docker exec -it sql_sprint_container /bin/sh
      ```

    - Once inside the container's shell, navigate to the directory containing the database file:

      ```sh
      cd /path/to/database
      ```

      *(Replace `/path/to/database` with the actual path inside the container.)*

    - Open the SQLite database:

      ```sh
      sqlite3 story02.db
      ```

    - You can now run SQL queries directly on the `story02.db` database.

5. **Running Your SQL Scripts:**

    - Inside the container, you can execute your SQL scripts against the prefilled database:

      ```sh
      sqlite3 story02.db < your_task_file.sql
      ```

    - Alternatively, you can copy your `.sql` files into the container and execute them.

6. **Exiting the Container Shell:**

    - When you're done, type `exit` to leave the container's shell.

#### Alternative: Accessing the Database from Your Host Machine

If the Docker container exposes the database file to a shared volume, you can access the SQLite database directly from your host machine.

1. **Run the Docker Container with Volume Mapping:**

    - Start the container and map a directory from the container to your host:

      ```sh
      docker run -d \
        --name sql_sprint_container \
        -v $(pwd)/data:/data \
        sql_sprint_image
      ```

        - This command maps the `/data` directory inside the container to a `data` directory in your current host directory.

2. **Access the Database File:**

    - The `story02.db` database file will be available in the `data` directory on your host machine.

    - You can interact with it using SQLite on your host:

      ```sh
      sqlite3 data/story02.db
      ```

3. **Begin Working on Tasks:**

    - Execute your SQL scripts against the `story02.db` database:

      ```sh
      sqlite3 data/story02.db < your_task_file.sql
      ```

For this bootcamp, you will work in the `sprint-sql` repository, so create it first and add your generated files into it. This repository will store all your bootcamp solutions.

## Important Notes:

    - Do not modify the structure of the prefilled database unless instructed.
    - If you encounter any issues, reach out to your instructor or TA for assistance.

### Resources

- [SQL Tutorial](https://www.w3schools.com/sql/)
- [SQLite Documentation](https://sqlite.org/docs.html)
- [Docker Basics](https://docs.docker.com/get-started/)

---