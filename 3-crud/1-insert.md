# INSERT

```sql
INSERT INTO employees (
    first_name, 
    last_name, 
    description, 
    birth_date, 
    hire_date
)
VALUES (
    'John', 
    'Doe', 
    'Employee description goes here.', 
    '1990-01-01', 
    '2022-01-01'
);
```
Or multi-row INSERT statement:

```sql
INSERT INTO employees (first_name, last_name)
VALUES ('First Name 1', 'Last Name 1'),
        ('First Name 2', 'Last Name 2'),
        ('First Name 3', 'Last Name 3');
```

Or insert values returned by a query:

```sql
INSERT INTO <table_name> (<column_names>)
SELECT <query>;
```


## MySQL
- [Insert Docs](https://dev.mysql.com/doc/refman/8.0/en/insert.html)

## PostgreSQL
- [Insert Docs](https://www.postgresql.org/docs/current/sql-insert.html)

## Microsoft SQL Server
- [Insert Docs](https://learn.microsoft.com/en-us/sql/t-sql/statements/insert-transact-sql?view=sql-server-ver16)

## SQLite
- [Insert Docs](https://www.sqlite.org/lang_insert.html)


