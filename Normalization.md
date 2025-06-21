# Normalization in Database

Normalization is the process of organizing data in a database to reduce redundancy and improve data integrity. It involves decomposing tables into smaller, related tables and defining relationships between them.

## Purpose of Normalization
Normalization aims to eliminate data anomalies, such as insertion, update, and deletion anomalies, by ensuring that each piece of data is stored in only one place. This helps maintain data consistency and reduces the risk of data corruption.


## The diffrence between Normalization and Database Mapping ?
**Normalization** focuses on organizing data within a database to minimize redundancy and ensure data integrity, 
while **database mapping** involves translating an entity-relationship model into a relational schema, defining how entities, attributes, and relationships are represented in tables and columns.


## 1st Normal Form (1NF)
1NF requires that all attributes in a table contain only atomic (indivisible) values and that each record is unique. This means that:

## 2nd Normal Form (2NF)
2NF builds on 1NF by ensuring that all non-key attributes are fully functionally dependent on the primary key. This means that:


## 3rd Normal Form (3NF)
3NF builds on 2NF by ensuring that all non-key attributes are not only fully functionally dependent on the primary key but also independent of each other.


## Example of Normalization
### Initial Table

| OrderID | CustomerName | ProductName | Quantity | Price |
|---------|---------------|-------------|----------|-------|
| 1       | John Doe     | Widget A    | 10       | 5.00  |
| 2       | Jane Smith   | Widget B    | 5        | 10.00 |
| 3       | John Doe     | Widget C    | 2        | 15.00 |

### 1st Normal Form (1NF)

| OrderID | CustomerName | ProductName | Quantity | Price |
|---------|---------------|-------------|----------|-------|
| 1       | John Doe     | Widget A    | 10       | 5.00  |
| 2       | Jane Smith   | Widget B    | 5        | 10.00 |
| 3       | John Doe     | Widget C    | 2        | 15.00 |

### 2nd Normal Form (2NF)
| OrderID | CustomerID | ProductID | Quantity | Price |
|---------|-------------|-----------|----------|-------|
| 1       | 1           | 1         | 10       | 5.00  |
| 2       | 2           | 2         | 5        | 10.00 |
| 3       | 1           | 3         | 2        | 15.00 |


### 3rd Normal Form (3NF)
| OrderID | CustomerID | ProductID | Quantity | Price |
|---------|-------------|-----------|----------|-------|
| 1       | 1           | 1         | 10       | 5.00  |
| 2       | 2           | 2         | 5        | 10.00 |
| 3       | 1           | 3         | 2        | 15.00 |
### Customer Table
| CustomerID | CustomerName |
|-------------|---------------|
| 1           | John Doe     |
| 2           | Jane Smith   |

### Product Table
| ProductID | ProductName |
|-------------|-------------|
| 1           | Widget A    |
| 2           | Widget B    |
| 3           | Widget C    |

## Summary
Normalization is a crucial process in database design that helps eliminate data redundancy and maintain data integrity. By organizing data into smaller, related tables and defining relationships between them, normalization ensures that each piece of data is stored in only one place, reducing the risk of data anomalies and corruption. The three normal forms (1NF, 2NF, and 3NF) provide a structured approach to achieving this goal, making databases more efficient and reliable.