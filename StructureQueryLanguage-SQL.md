# Structured Query Language < SQL >

## **Definition:**
SQL is a standardized programming language used to manage and manipulate relational databases.
It allows users to perform various operations such as querying data, updating records, inserting new data, and deleting existing data.


## Types of SQL Statements:
1. **Data Definition Language (DDL):**
   - Used to define the structure of the database, including creating, altering, and dropping tables.
		- Structures the database schema and objects.
		- Objects include tables, indexes, and views.
		- Examples: `CREATE`, `ALTER`, `DROP`, `TRUNCATE`, `RENAME`.

2. **Data Manipulation Language (DML):**
	- Used to manipulate data within the database, including inserting, updating, and deleting records.
		- Examples: `INSERT`, `UPDATE`, `DELETE`.

3. **Data Query Language (DQL):**
	- Used to query and retrieve data from the database.
		- Examples: `SELECT`.
		- Select -> Join , Group By , agregate functions, etc.

4. **Transaction Control Language (TCL):**
	- Used to manage transactions in the database, ensuring data integrity and consistency.
		- Examples: `COMMIT`, `ROLLBACK`, `SAVEPOINT`.

5. **Data Control Language (DCL):**
	- Used to control access to data in the database, including granting and revoking permissions.
		- Examples: `GRANT`, `REVOKE`.


## Integrity

1. Domain Integrity:
   - Ensures that data entered into the database adheres to specific rules or constraints.
   - Examples: Data types, value ranges, and formats.

2. Entity Integrity:
	- Ensures that each row in a table is uniquely identifiable.
	- Examples: Primary keys, unique constraints.

3. Referential Integrity:
	- Ensures that relationships between tables remain consistent.
	- Examples: Foreign keys, cascading updates/deletes.



# SQL Syntax:

## DDL (Data Definition Language):
```sql

-- Create a new table
CREATE TABLE table_name (
	column1 datatype [constraints],
	column2 datatype [constraints],
	...
);

-- Alter an existing table
ALTER TABLE table_name
ADD column_name datatype [constraints];


-- Drop a table
DROP TABLE table_name;


-- Rename a table
RENAME TABLE old_table_name TO new_table_name;


-- Truncate a table (remove all rows)
TRUNCATE TABLE table_name;
```

## DML (Data Manipulation Language):
```sql

-- Insert data into a table
INSERT INTO table_name (column1, column2, ...)
VALUES (value1, value2, ...);

-- Update existing data in a table
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;

-- Delete data from a table
DELETE FROM table_name
WHERE condition;
```

## DQL (Data Query Language):
```sql
-- Select data from a table
SELECT column1, column2, ...
FROM table_name
WHERE condition
ORDER BY column1, column2, ...
LIMIT number_of_rows;


-- Select all columns from a table

SELECT *
FROM table_name
WHERE condition
ORDER BY column1, column2, ...
LIMIT number_of_rows;
```

```sql

-- Select distinct values from a column
SELECT DISTINCT column_name
FROM table_name
WHERE condition
ORDER BY column_name
LIMIT number_of_rows;
```

```sql

-- Select data with aggregate functions
SELECT aggregate_function(column_name)
FROM table_name
WHERE condition
GROUP BY column_name
ORDER BY column_name
LIMIT number_of_rows;
```
```sql
-- Select data with joins
SELECT column1, column2, ...
FROM table1
JOIN table2 ON table1.common_column = table2.common_column
WHERE condition
ORDER BY column1, column2, ...
LIMIT number_of_rows;
```
```sql
-- Select data with subqueries
SELECT column1, column2, ...
FROM table_name
WHERE column1 IN (SELECT column1 FROM another_table WHERE condition)
ORDER BY column1, column2, ...
LIMIT number_of_rows;
```

## TCL (Transaction Control Language):
```sql
-- Commit a transaction
COMMIT;


-- Rollback a transaction
ROLLBACK;


-- Savepoint in a transaction
SAVEPOINT savepoint_name;


-- Release a savepoint
RELEASE SAVEPOINT savepoint_name;
```


## DCL (Data Control Language):
```sql
-- Grant permissions to a user
GRANT permission_type ON object TO user_name;


-- Revoke permissions from a user
REVOKE permission_type ON object FROM user_name;
```

