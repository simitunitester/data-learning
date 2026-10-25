# data-learning

My notes while learning SQL, Python, Power BI and data engineering.

Things I want to revise later are marked with ⭐ REVISE.

## SQL

### Column Selection

```sql
SELECT column_1,
       column_2
FROM table_1;
```

- We use `SELECT` to specify which columns to retrieve and `FROM` to specify the table to retrieve from.
- `SELECT column_1`: selects one column
- `SELECT column_1, column_2`: selects multiple columns
- `SELECT *`: selects all columns

### Finding Unique Values

```sql
SELECT DISTINCT column_name
FROM table_name;
```

- We use `DISTINCT` to retrieve only unique values from a column, eliminating duplicates.
- `DISTINCT` is placed immediately after `SELECT`.

### Column Aliasing

```sql
SELECT column_1 AS alias_name,
       column_2
FROM table_1;
```

- The `AS` keyword assigns temporary names to columns in query results to improve readability.
- The alias appears in column headers but doesn't change the original database column name.
- Effective aliases should be descriptive, consistent, and use snake_case convention for best practices.

### SQL Style Conventions

- Write SQL keywords in uppercase (`SELECT`, `FROM`, `ORDER BY`) to distinguish them from table and column names.
- This convention improves code readability and makes queries easier to understand and maintain.

### SQL Flavors

- Different database systems use SQL flavors with the same core syntax but minor differences in specific features.
- What you learn in one system transfers easily to others, making SQL skills broadly applicable across platforms.

### Client-Server Architecture

- Database servers store and manage databases, while database clients connect to servers and send queries.
- Multiple users can connect simultaneously to the same database server through various types of clients including web applications and desktop software.

### SQL Query Basics

- A SQL query retrieves data from a database using the `SELECT` and `FROM` keywords.

```sql
SELECT column_1,
       column_2
FROM table_name;
```

- `SELECT` specifies which columns to retrieve (`*` for all columns).
- `FROM` specifies which table to query.
- `;` is the statement terminator that marks the end of a query.

### Data Aggregation

- Data aggregation is the operation of summarizing data by applying functions (like SUM, AVG, COUNT) to columns to produce single values.
- Data aggregation reveals insights and patterns that are difficult to recognize by examining raw data alone.

### Summarizing Data in SQL

- To apply summary operations in SQL, use aggregate functions within a SELECT statement:

```sql
SELECT COUNT(column_1) AS metric_1,
       SUM(column_2)   AS metric_2
FROM table_name;
```

- The `AS` keyword assigns a temporary name (alias) to a column, making output more readable.
- Calculate multiple summary values in one query by listing aggregate functions separated by commas.
- You can also calculate just one summary value by using a single aggregate function.

### Summary Operations

- `SUM()`: Calculates the total of all values in a column
- `AVG()`: Calculates the average value in a column
- `MIN()`: Finds the minimum value in a column
- `MAX()`: Finds the maximum value in a column
- `COUNT()`: Counts the number of rows or values
- `COUNT(DISTINCT column)`: Counts the number of unique values

### Design Framework

- Thinking through your query before writing code is one of the most effective habits of successful data analysts.
- To effectively design a data aggregation operation, answer two key questions:
  1. Which column do we wish to summarize? Select the column containing values relevant to your question.
  2. Which summary operation do we wish to apply? Choose the appropriate operation based on the insight you need.
