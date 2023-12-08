# Rename Column

## MySQL

```sql
ALTER TABLE your_table_name
CHANGE COLUMN old_column_name new_column_name new_data_type;
```

- [Alter Table Docs](https://dev.mysql.com/doc/refman/8.0/en/alter-table.html)

## PostgreSQL

```sql
ALTER TABLE your_table_name
RENAME COLUMN old_column_name TO new_column_name;
```

- [Alter Table Docs](https://www.postgresql.org/docs/current/sql-altertable.html)

## Microsoft SQL Server

```sql
EXEC sp_rename 'your_table_name.old_column_name', 'new_column_name', 'COLUMN';
```

- [Ranem Column Docs](https://learn.microsoft.com/en-us/sql/relational-databases/tables/rename-columns-database-engine?view=sql-server-ver16)

## SQLite

```sql
ALTER TABLE your_table_name 
RENAME COLUMN old_column_name TO new_column_name;
```

- [Alter Table Docs](https://www.sqlite.org/lang_altertable.html)