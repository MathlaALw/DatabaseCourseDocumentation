# Subquery and Union


## What is subquery?

**Definition**: A subquery is a query nested inside another SQL query. It can be used to retrieve data that will be used in the main query or to filter results based on conditions derived from another query.

**Purpose**: Subqueries allow for more complex queries by enabling the use of results from one query as input for another. They can be used in various clauses such as `SELECT`, `FROM`, `WHERE`, and `HAVING`.

**Example**: 
```sql
SELECT employee_id, first_name, last_name
FROM employees
WHERE department_id IN (SELECT department_id FROM departments WHERE location = 'New York');
```

This query retrieves the employee IDs, first names, and last names of employees who work in departments located in New York. The subquery `(SELECT department_id FROM departments WHERE location = 'New York')` returns a list of department IDs that are then used in the main query's `WHERE` clause to filter employees.

## What is Union?

**Definition**: The `UNION` operator in SQL is used to combine the results of two or more `SELECT` statements into a single result set. It removes duplicate rows from the combined result.

**Purpose**: The `UNION` operator allows you to retrieve data from multiple tables or queries and present it as a single unified result set. It is useful for combining similar data from different sources.

**Example**: 
```sql
SELECT first_name, last_name FROM employees
UNION
SELECT first_name, last_name FROM contractors;
```

This query retrieves the first and last names of employees and contractors, combining the results into a single list. Duplicate names will be removed from the final result set.

## What is Union All?

**Definition**: The `UNION ALL` operator in SQL is similar to the `UNION` operator, but it does not remove duplicate rows from the combined result set. It combines the results of two or more `SELECT` statements, including all duplicates.

**Purpose**: The `UNION ALL` operator allows you to retrieve data from multiple tables or queries while preserving all rows, including duplicates. It is useful when you want to see all occurrences of data without filtering out duplicates.

**Example**: 
```sql

SELECT first_name, last_name FROM employees
UNION ALL
SELECT first_name, last_name FROM contractors;
```

This query retrieves the first and last names of employees and contractors, combining the results into a single list without removing any duplicates. If an employee and a contractor have the same name, both will appear in the final result set.

## What is Intersect?

**Definition**: The `INTERSECT` operator in SQL is used to return the common rows from two or more `SELECT` statements. It retrieves only the rows that are present in both result sets.

**Purpose**: The `INTERSECT` operator allows you to find the intersection of two or more result sets, returning only the rows that are identical in all specified columns.

**Example**: 
```sql

SELECT first_name, last_name FROM employees
INTERSECT
SELECT first_name, last_name FROM contractors;
```

This query retrieves the first and last names that are common to both employees and contractors. Only those names that appear in both result sets will be included in the final output.

## What is Except?

**Definition**: The `EXCEPT` operator in SQL is used to return the rows from the first `SELECT` statement that are not present in the second `SELECT` statement. It effectively subtracts one result set from another.

**Purpose**: The `EXCEPT` operator allows you to find the difference between two result sets, returning only the rows that exist in the first set but not in the second.

**Example**: 
```sql

SELECT first_name, last_name FROM employees
EXCEPT
SELECT first_name, last_name FROM contractors;
```

This query retrieves the first and last names of employees that are not present in the contractors list. It effectively filters out any names that appear in both sets, returning only those unique to the employees.

