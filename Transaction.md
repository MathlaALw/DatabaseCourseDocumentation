# Transaction in SQL

# **Definition:**
A transaction is a sequence of one or more SQL operations that are executed as a single unit of work. It ensures that either all operations are completed successfully or none are applied, maintaining the integrity of the database.

# **Purpose:**

Transactions are used to ensure data integrity and consistency in a database. They allow multiple operations to be grouped together, so that if one operation fails, the entire transaction can be rolled back, preventing partial updates that could lead to data corruption.

# **Example:**
```sql

BEGIN TRANSACTION;
UPDATE accounts SET balance = balance - 100 WHERE account_id = 1;
UPDATE accounts SET balance = balance + 100 WHERE account_id = 2;
COMMIT;
```
~~Note~~:
The instractions within the transaction block will only be applied if all operations are successful. If any operation fails, the transaction can be rolled back to its initial state, ensuring that no changes are made to the database.


