# Employee Database Operations

This repository contains SQL scripts for managing an `employee` table in a PostgreSQL database. The scripts include commands for creating the table, inserting data, updating records, deleting records, and querying the data.

### Table Creation

The following SQL script creates an `employee` table with the following columns:

- `id`: A unique identifier for each employee (auto-incremented primary key).
- `name`: The name of the employee (cannot be null).
- `email`: The email address of the employee.
- `birthday`: The birthdate of the employee.

```sql
CREATE TABLE employee (
  id SERIAL PRIMARY KEY,
  name VARCHAR(50) NOT NULL,
  email VARCHAR(100),
  birthday DATE
);
```
### Insert Operations
The script inserts multiple records into the employee table. Here are some examples:

```sql
INSERT INTO employee (name, email, birthday) VALUES ('Jobi Solan', 'jsolan0@friendfeed.com', '1992-08-29');
INSERT INTO employee (name, email, birthday) VALUES ('Chlo Holde', 'cholde1@wp.com', '1980-06-17');
INSERT INTO employee (name, email, birthday) VALUES ('Lonni Gethin', 'lgethin2@ebay.co.uk', '1986-04-15');

-- Additional insert statements...
```

Update Operations
The script includes update statements to modify existing records in the employee table. For example:

```sql

UPDATE employee SET name = 'Melike Göz', email = 'melike@goz.com', birthday = '1993-03-04' WHERE id = 1;
UPDATE employee SET name = 'Ahmet Göz', email = 'ahmet@goz.com', birthday = '1993-09-18' WHERE id = 2;
-- Additional update statements...
```
### Delete Operations
The script contains delete statements to remove records from the employee table based on specific conditions. For example:

```sql

DELETE FROM employee WHERE id = 6;
DELETE FROM employee WHERE id = 7 AND name LIKE 'Nessa%';
DELETE FROM employee WHERE id = 8;
-- Additional delete statements...
```
### Query Operations
Finally, the script provides a query to retrieve all records from the employee table, ordered by id:

```sql

SELECT * FROM employee ORDER BY id;
```
## How to Use
Ensure you have a PostgreSQL database set up and accessible.
Run the table creation script to set up the employee table.
Execute the insert, update, and delete scripts as needed.
Use the query scripts to retrieve and analyze the data.
