# Create Trigger

## MySQL

```sql
-- Create a trigger
CREATE TRIGGER your_trigger_name
AFTER INSERT ON your_table
FOR EACH ROW
BEGIN
    -- Your trigger logic goes here
    -- For example, you can insert into another table
    INSERT INTO your_audit_table (column1, column2)
    VALUES (NEW.column1, NEW.column2);
END;
```

- [SP Docs](https://dev.mysql.com/doc/refman/8.0/en/trigger-syntax.html)

## PostgreSQL

```sql
-- Create a function
CREATE OR REPLACE FUNCTION your_trigger_function()
RETURNS TRIGGER AS $$
BEGIN
    -- Your trigger logic goes here
    -- For example, you can insert into another table
    INSERT INTO your_audit_table (column1, column2)
    VALUES (NEW.column1, NEW.column2);
    
    RETURN NEW;
END;
$$ LANGUAGE plpgsql;

-- Create a trigger
CREATE TRIGGER your_trigger_name
AFTER INSERT OR UPDATE ON your_table
FOR EACH ROW
EXECUTE FUNCTION your_trigger_function();
```

- [SP Docs](https://www.postgresql.org/docs/current/sql-createtrigger.html)

## Microsoft SQL Server

```sql
-- Create a trigger
CREATE TRIGGER your_trigger_name
ON your_table
AFTER INSERT
AS
BEGIN
    -- Your trigger logic goes here
    -- For example, you can insert into another table
    INSERT INTO your_audit_table (column1, column2)
    SELECT column1, column2
    FROM INSERTED;
END;
```

- [SP Docs](https://learn.microsoft.com/en-us/sql/t-sql/statements/create-trigger-transact-sql?view=sql-server-ver16)

## SQLite


```sql
-- Create a trigger
CREATE TRIGGER your_trigger_name
AFTER INSERT ON your_table
BEGIN
    -- Your trigger logic goes here
    -- For example, you can insert into another table
    INSERT INTO your_audit_table (column1, column2)
    VALUES (NEW.column1, NEW.column2);
END;
```

- [SP Docs](https://www.sqlite.org/lang_createtrigger.html)
