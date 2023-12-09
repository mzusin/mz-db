# Create Stored Procedure

## MySQL

```sql
DELIMITER //
CREATE PROCEDURE get_employee_count()
BEGIN
    SELECT COUNT(*) FROM employees;
END //
DELIMITER ;
```

- [SP Docs](https://dev.mysql.com/doc/refman/8.0/en/create-procedure.html)

## PostgreSQL

```sql
CREATE OR REPLACE PROCEDURE proj_get_all_projects()
AS $$
BEGIN
    SELECT 
        project_id,
        project_title,
        project_desc,
        project_color,
        project_order
    FROM plan_project;
END;
$$ LANGUAGE plpgsql;

-- Execute:
-- CALL get_all_projects();
```

```sql
CREATE OR REPLACE FUNCTION get_employee_count()
RETURNS INTEGER AS $$
DECLARE
    count INTEGER;
BEGIN
    SELECT COUNT(*) INTO count FROM employees;
    RETURN count;
END;
$$ LANGUAGE plpgsql;
```

- [SP Docs](https://www.postgresqltutorial.com/postgresql-plpgsql/postgresql-create-procedure/)

## Microsoft SQL Server

```sql
CREATE PROCEDURE get_employee_count
AS
BEGIN
    SELECT COUNT(*) FROM employees;
END;
```

- [SP Docs](https://learn.microsoft.com/en-us/sql/relational-databases/stored-procedures/create-a-stored-procedure?view=sql-server-ver16)

## SQLite
SQLite does not support stored procedures.
