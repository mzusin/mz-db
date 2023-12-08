# Create Table with Foreign Key

## MySQL

```sql
-- Create the referenced table
CREATE TABLE departments (
    department_id INT AUTO_INCREMENT PRIMARY KEY,
    department_name VARCHAR(50)
);

-- Create the table with a foreign key reference
CREATE TABLE employees (
    employee_id INT AUTO_INCREMENT PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    department_id INT NOT NULL,
    FOREIGN KEY (department_id) REFERENCES departments(department_id)
);
```

- [Foreign Key Docs](https://dev.mysql.com/doc/refman/8.0/en/create-table-foreign-keys.html)

## PostgreSQL

```sql
-- Create the referenced table
CREATE TABLE departments (
    department_id SERIAL PRIMARY KEY,
    department_name VARCHAR(50)
);

-- Create the table with a foreign key reference
CREATE TABLE employees (
    employee_id SERIAL PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    department_id INTEGER NOT NULL REFERENCES departments(department_id)
);
```

- [Foreign Key Docs](https://www.postgresql.org/docs/current/tutorial-fk.html)

## Microsoft SQL Server

```sql
-- Create the referenced table
CREATE TABLE departments (
    department_id INT AUTO_INCREMENT PRIMARY KEY,
    department_name VARCHAR(50)
);

-- Create the table with a foreign key reference
CREATE TABLE employees (
    employee_id INT AUTO_INCREMENT PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    department_id INT NOT NULL,
    FOREIGN KEY (department_id) REFERENCES departments(department_id)
);
```

- [Foreign Key Docs](https://learn.microsoft.com/en-us/sql/relational-databases/tables/create-foreign-key-relationships?view=sql-server-ver16)

## SQLite

```sql
-- Create the referenced table
CREATE TABLE departments (
    department_id INTEGER PRIMARY KEY,
    department_name TEXT NOT NULL
);

-- Create the table with a foreign key reference
CREATE TABLE employees (
    employee_id INTEGER PRIMARY KEY,
    first_name TEXT NOT NULL,
    last_name TEXT NOT NULL,
    department_id INTEGER NOT NULL,
    FOREIGN KEY (department_id) REFERENCES departments(department_id)
);
```

- [Foreign Key Docs](https://www.sqlite.org/foreignkeys.html)
