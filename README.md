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
