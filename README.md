# My Project: Persistence Service

## Goal
In class, we've learned about Databases and their design. Furthermore, you've been shown how a project-level persistence service works. In this final project, you are going to be asked to bring up a project.

## Submission Instructions
Please name the filename to the following: `[group 10] - SENG8070 - Final Assignment`

: `group10 - SENG8070 - Final Assignment`

Please submit your assignment to eConestoga. The assignment that will be considered for grades is the one that is submitted into eConestoga.

**Please remove all `node_modules` folders as this makes the project huge.**

## Assignment Instructions

### The Project
The task before you is to create a working system that satisfies the bookstore you designed a database for in the midterm. It should satisfy all criteria.

### Criteria
You are designing a system for an online bookstore. The bookstore sells physical books, e-books, and audiobooks. Customers can browse the catalog, make purchases, and leave reviews. Authors and publishers are also part of the system.

You are responsible for coming up with the data that you should capture; however, the bookstore has given a list of requirements that you must include:

- Power writers (authors) with more than X books in the same genre published within the last X years.
- Loyal Customers who have spent more than X dollars in the last year.
- Well-reviewed books that have a better user rating than average.
- The most popular genre by sales.
- The 10 most recent posted reviews by Customers.

### The Assignment (Part 1)
Your assignment submission will be a working project. In it, you will:

- Include a responsibility list of who in your group is responsible for which portion of the project.
- Have a working database complete with all the tables and columns.
- Implement CRUD functions to interact with every single table.
- Write unit tests that cover the CRUD operations.
- Write integration tests that cover the CRUD operations.
- **Bonus (3pts)**: Create a migration so that there are at least 3 rows of data in each table.
- Include an Entity Relations diagram of your database design.

### The Technical Requirements
- The project will be a TypeScript (not JavaScript) based project.
- The project will use TypeORM.
- The project needs to be usable in a containerized manner.

### The Presentation (Part 2)
There is a presentation that your group will need to make. In this presentation, I am looking for you to present your problem set, present your solution, and emphasize how your implementation helps ensure a high-quality system that will persist the data for our client.

Your presentation should be no more than 15 minutes long.

## Getting Started

### Requirements
You will need NPM and Node installed on your local machine. It is highly recommended that you use an environment manager to prevent pollution of your local system.

### Quickest Way
Navigate to the Download Page of Node.js, download the correct package for your system, and install.

### Industry Standard Way

#### Linux/macOS
I highly recommend NVM. Read about the details on the NVM project page.

#### Windows
Setting up development for Windows is a little bit more complicated. You will likely need:
- A terminal (e.g., zsh or bash)
- SSH
- Git

For the terminal, I recommend zsh or bash. Here is a tutorial on setting up zsh on your Windows Machine.

After that, the environment manager I recommend for Windows is nvm-windows.

### Starting Development
Validate that you have Node and NPM:


### Authors Table

| Attribute | Type               |
|-----------|--------------------|
| author_id | SERIAL PRIMARY KEY |
| name      | VARCHAR(255)       |
| bio       | TEXT               |

### Publishers Table

| Attribute    | Type               |
|--------------|--------------------|
| publisher_id | SERIAL PRIMARY KEY |
| name         | VARCHAR(255)       |
| address      | TEXT               |

### Genres Table

| Attribute | Type               |
|-----------|--------------------|
| genre_id  | SERIAL PRIMARY KEY |
| name      | VARCHAR(255)       |

### Books Table

| Attribute      | Type               |
|----------------|--------------------|
| book_id        | SERIAL PRIMARY KEY |
| title          | VARCHAR(255)       |
| genre_id       | INT                |
| price          | DECIMAL(10,2)      |
| format         | VARCHAR(20)        |
| author_id      | INT                |
| publisher_id   | INT                |
| published_date | DATE               |
| stock_quantity | INT                |

### Customers Table

| Attribute   | Type               |
|-------------|--------------------|
| customer_id | SERIAL PRIMARY KEY |
| name        | VARCHAR(255)       |
| email       | VARCHAR(255)       |
| total_spent | DECIMAL(10,2)      |

### Reviews Table

| Attribute    | Type               |
|--------------|--------------------|
| review_id    | SERIAL PRIMARY KEY |
| book_id      | INT                |
| customer_id  | INT                |
| rating       | INT                |
| review_text  | TEXT               |
| review_date  | DATE               |

```bash
node -v
npm -v



