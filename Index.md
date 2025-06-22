# Index in SQL

## What is an Index?

An index in SQL is a database object that improves the speed of data retrieval operations on a table at the cost of additional space and slower write operations. It works similarly to an index in a book, allowing the database engine to find rows more quickly without scanning the entire table.


## Why Use an Index?

Indexes are used to:
- **Speed up data retrieval**: They allow the database to find rows faster, especially in large tables.

- **Improve query performance**: Queries that filter or sort data can run much faster with appropriate indexes.

- **Enforce uniqueness**: Unique indexes ensure that no two rows have the same value in a specified column or set of columns.

## Types of Indexes

### 1. Clustered Index

A clustered index determines the physical order of data in a table. 
There can be only one clustered index per table, and it is usually created on the primary key. 
When a clustered index is created, the table's data rows are stored in the order of the indexed column(s).

- if i have a table without **PK** it will stored in heap file in -**Databage**- the
  data is **not ordered**. so the search will be **slow**. they apply **table scan**  that will access all the pages to find the data.

- if i have a table with **PK** it will stored in **B-Tree** structure. 
  the data is **ordered**. so the search will be **fast**. they apply **Page scan** that will access only the pages that contain the data.

- the **PK** allways create a **clustered index**. 

**Syntax to create a clustered index:**
```sql
CREATE CLUSTERED INDEX index_name
ON table_name (column_name);
```
### 2. Non-Clustered Index

A non-clustered index is a separate structure from the data rows. 
It contains a sorted list of references to the actual data rows. 
A table can have multiple non-clustered indexes, and they are often used to speed up queries that filter or sort on columns that are not part of the clustered index.

**Syntax to create a non-clustered index:**
```sql
CREATE NONCLUSTERED INDEX index_name
ON table_name (column_name);
```


~~Note:~~
- **its possible to create a non-clustered index on all the columns of the table but it will take more space and it will be slower to update the index when the data changes.**
- **PK is always a clustered index** but you can create a non-clustered index on the same column if needed.
- **Primary key   -> Constraint -> Clustered Index**
- **Unique        -> Constraint -> nonclutered index**





