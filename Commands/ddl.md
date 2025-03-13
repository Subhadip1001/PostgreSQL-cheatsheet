# Data Definition Language (DDL) Commands in PostgreSQL

## 1. Create a Database
```sql
CREATE DATABASE <DATABASE_NAME>;
```

## 2. Drop a Database
```sql
DROP DATABASE <DATABASE_NAME>;
```

## 3. Create a Table
```sql
CREATE TABLE <TABLE_NAME> (
    column1 datatype constraints,
    column2 datatype constraints,
    ...
);
```
### Example:
```sql
CREATE TABLE EMPLOYEE (
    Eid INT PRIMARY KEY,
    Ename VARCHAR(50) NOT NULL,
    Email VARCHAR(100) UNIQUE NOT NULL,
    Salary INT NOT NULL,
    Joining_Date DATE DEFAULT CURRENT_DATE
);
```

## 4. Drop a Table
```sql
DROP TABLE <TABLE_NAME>;
```

## 5. Alter a Table
### Add a Column
```sql
ALTER TABLE <TABLE_NAME> ADD COLUMN column_name datatype;
```
### Modify a Column
```sql
ALTER TABLE <TABLE_NAME> ALTER COLUMN column_name TYPE new_datatype;
```
### Rename a Column
```sql
ALTER TABLE <TABLE_NAME> RENAME COLUMN old_name TO new_name;
```
### Drop a Column
```sql
ALTER TABLE <TABLE_NAME> DROP COLUMN column_name;
```

## 6. Truncate a Table (Remove all Data without Dropping Table)
```sql
TRUNCATE TABLE <TABLE_NAME>;
```

## 7. Show Table Structure
```sql
\d <TABLE_NAME>
```

