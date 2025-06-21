# Functions in SQL

**Definition**: Functions in SQL are predefined operations that can be used to perform calculations, manipulate data, or return specific values. They can be categorized into various types, including aggregate functions, string functions, date functions, and mathematical functions.

**Purpose**: Functions are used to simplify complex operations, enhance query capabilities, and improve code readability. They allow users to perform operations on data without needing to write extensive code.

## Types of Functions in SQL:

### Bildin Functions:
- **Definition**: Built-in functions are pre-defined functions provided by the SQL language that can be used directly in queries.
- **Purpose**: They simplify common operations such as string manipulation, date calculations, and mathematical computations.

- **Type of Built-in Functions**:
  - **String Functions**: Used to manipulate string data.
	- Examples: `UPPER()`, `LOWER()`, `SUBSTRING()`, `TRIM()`.
  - **Date Functions**: Used to perform operations on date and time values.
	- Examples: `GETDATE()`, `DATEADD()`, `DATEDIFF()`.
  - **Mathematical Functions**: Used to perform mathematical calculations.
	- Examples: `ABS()`, `ROUND()`, `CEILING()`, `FLOOR()`.
  - **Aggregate Functions**: Used to perform calculations on a set of values and return a single value.
	- Examples: `COUNT()`, `SUM()`, `AVG()`, `MIN()`, `MAX()`.

### User-Defined Functions (UDFs):

- **Definition**: User-defined functions are custom functions created by users to perform specific operations that are not available as built-in functions.

- **Purpose**: UDFs allow users to encapsulate complex logic and reuse it across multiple queries or applications, enhancing code modularity and maintainability.

- **Types of User-Defined Functions**:
  - **Scalar Functions**: Return a single value based on input parameters.
	- Example: A function that calculates the total price of an order based on quantity and unit price.
  - **Inline Table-Valued Functions**: Return a table as a result set, allowing for more complex data retrieval.
	- Example: A function that retrieves all orders for a specific customer.
  - **Multi-Statement Table-Valued Functions**: Similar to inline functions but can contain multiple statements and logic to build the result set.
	- Example: A function that calculates sales statistics for a specific period and returns a table with multiple columns.

## Variables in SQL:

### Types of Variables:

1. **Local Variables**:
   - **Definition**: Local variables are temporary storage locations that can hold data during the execution of a SQL script or stored procedure.
   - **Purpose**: They are used to store intermediate results, control flow values, or parameters within a specific scope.
   - **Example**: 
	 ```sql
	 DECLARE @TotalSales INT;
	 SET @TotalSales = (SELECT SUM(sales_amount) FROM sales WHERE sale_date = GETDATE());
	 ```

2. **Global Variables**:
   - **Definition**: Global variables are predefined variables that are accessible throughout the entire SQL session or across multiple sessions.
   - **Purpose**: They provide information about the current session, server, or environment.
   - **Example**: 
	 ```sql
	 SELECT @@VERSION; -- Returns the version of the SQL Server instance
	 SELECT @@ROWCOUNT; -- Returns the number of rows affected by the last statement
	 SELECT @@ERROR; -- Returns the error number for the last executed statement
	 SELECT @@IDENTITY; -- Returns the last identity value generated in the current session
	 SELECT @@SERVERNAME; -- Returns the name of the SQL Server instance
	 ```
	 