# SQL

**SQL** is a database computer language designed for the retrieval and management of data in a relational database. **SQL** stands for **Structured Query Language**.  

SQL is one of the most widely used query language over the databases: 

- Allows users to access data in the relational database management systems.

- Allows users to describe the data.

- Allows users to define the data in a database and manipulate that data.

- Allows to embed within other languages using SQL modules, libraries & pre-compilers.

- Allows users to create and drop databases and tables.

- Allows users to create view, stored procedure, functions in a database.

- Allows users to set permissions on tables, procedures and views. 

## Relational databases  

It's important to have a model for what a relational database actually is.  

A relational database represents a collection of related (two-dimensional) tables. Each of the tables are similar to an Excel spreadsheet, with a fixed number of named columns (the attributes or properties of the table) and any number of rows of data.

## Syntax 

SQL is followed by a unique set of rules and guidelines called Syntax.  

All the SQL statements start with any of the keywords like SELECT, INSERT, UPDATE, DELETE, ALTER, DROP, CREATE, USE, SHOW and all the statements end with a semicolon (;).

To retrieve data from a SQL database, we need to write **SELECT** statements, which are often colloquially refered to as queries. A query in itself is just a statement which declares what data we are looking for, where to find it in the database, and optionally, how to transform it before it is returned.

```sql
-- Select query for a specific columns
SELECT column, another_column, …
FROM mytable;

-- Select query for all columns
SELECT * 
FROM mytable;
``` 

In order to filter certain results from being returned, we need to use a **WHERE** clause in the query. The clause is applied to each row of data by checking specific column values to determine whether it should be included in the results or not.

```sql
-- Select query with constraints
SELECT column, another_column, …
FROM mytable
WHERE condition
    AND/OR another_condition
    AND/OR …;
```

- `=, !=, < <=, >, >=` 
  - Standard numerical operators
- `BETWEEN … AND …`
  - Number is within range of two values (inclusive)
- `NOT BETWEEN … AND …`
  - Number is not within range of two values (inclusive)
- `IN (…)`
  - Number exists in a list
- `NOT IN (…)`
  - Number does not exist in a list
