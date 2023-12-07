# Create Table

```sql
CREATE TABLE your_table_name (
    column1 datatype1,
    column2 datatype2,
    column3 datatype3,
    -- add more columns as needed
);
```

## MySQL

```sql
CREATE TABLE employees (
    employee_id INT PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    birth_date DATE,
    hire_date DATE
);
```

- [Create Table Docs](https://dev.mysql.com/doc/refman/8.0/en/create-table.html)
- [Data Types Docs](https://dev.mysql.com/doc/refman/8.0/en/data-types.html)

## PostgreSQL

```sql
CREATE TABLE employees (
    employee_id serial PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    birth_date DATE,
    hire_date DATE
);
```

- [Create Table Docs](https://www.postgresqltutorial.com/postgresql-tutorial/postgresql-create-table/)
- [Data Types Docs](https://www.postgresql.org/docs/current/datatype.html)

## Microsoft SQL Server

```sql
CREATE TABLE employees (
    employee_id INT PRIMARY KEY,
    first_name NVARCHAR(50),
    last_name NVARCHAR(50),
    birth_date DATE,
    hire_date DATE
);
```

- [Create Table Docs](https://learn.microsoft.com/en-us/sql/t-sql/statements/create-table-transact-sql?view=sql-server-ver16)
- [Data Types Docs](https://learn.microsoft.com/en-us/sql/t-sql/data-types/data-types-transact-sql?view=sql-server-ver16)

## SQLite
 
```sql
CREATE TABLE employees (
    employee_id INTEGER PRIMARY KEY,
    first_name TEXT,
    last_name TEXT,
    birth_date DATE,
    hire_date DATE
);
```

- [Create Table Docs](https://www.sqlite.org/lang_createtable.html)
- [Data Types Docs](https://www.sqlite.org/datatype3.html)
