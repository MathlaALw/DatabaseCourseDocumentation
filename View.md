# View in SQL

**Definition**: 
A view in SQL is a virtual table that is based on the result of a query. It does not store data itself but provides a way to present data from one or more tables in a specific format or structure.

**Purpose**:
Views are used to simplify complex queries, encapsulate logic, and provide a layer of security by restricting access to specific columns or rows of data. They can also be used to present data in a more user-friendly manner.

**Creating a View**:
```sql
CREATE VIEW view_name AS
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```
**Example**:
```sql
CREATE VIEW employee_view AS
SELECT first_name, last_name, department
FROM employees
WHERE active = 1;
```
This example creates a view named `employee_view` that selects the first name, last name, and department of active employees from the `employees` table.

**Using a View**:
```sql
SELECT * FROM view_name;
```

**View Types**:
1. **Standard View**: A basic view that encapsulates a query.
   - Example: `SELECT * FROM employee_view;`
2. **Partitioned View**: A view that combines data from multiple tables or partitions.
   - Example: `SELECT * FROM partitioned_view;`
3. **Indexed View**: A view that has a unique clustered index, allowing it to be treated like a table.
   - Example: 
   ```sql
   CREATE UNIQUE CLUSTERED INDEX idx_employee_view ON employee_view (first_name, last_name);
   ```

5. **Encrypted View**: A view that is encrypted to protect sensitive data.
   - Example:
   ```sql
   CREATE VIEW encrypted_view WITH ENCRYPTION AS
   SELECT first_name, last_name FROM employees WHERE sensitive_data = 1;
   ```

