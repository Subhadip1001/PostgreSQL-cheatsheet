# Basic PostgreSQL Commands

## 1. Show All Databases
```sql
\list OR \l
```

## 2. Change Database
```sql
\c <Database Name>
```

## 3. Create a Database
```sql
CREATE DATABASE <DATABASE_NAME>;
```

## 4. Delete a Database
```sql
DROP DATABASE <DATABASE_NAME>;
```

## 5. Show Table Structure
```sql
\d <table_name>
```

## 6. Create a Table
```sql
CREATE TABLE <TABLE_NAME> (
    column1 datatype constraints,
    column2 datatype constraints,
    ...
);
```
### Example:
```sql
CREATE TABLE PERSON (
    ID INT PRIMARY KEY,
    NAME VARCHAR(30),
    CITY VARCHAR(20)
);
```

## 7. Insert Values into Table
```sql
INSERT INTO PERSON VALUES (101, 'SUBHADIP', 'KOLKATA');
```
### Insert Multiple Values
```sql
INSERT INTO PERSON VALUES
(104, 'RAHUL SHARMA', 'MUMBAI'),
(105, 'AMIT KUMAR', 'PUNE'),
(106, 'VIKAS SINGH', 'CHENNAI');
```

## 8. Read Data from Table
### Select All Columns
```sql
SELECT * FROM PERSON;
```
### Select Specific Columns
```sql
SELECT NAME FROM PERSON;
SELECT NAME, CITY FROM PERSON;
```
### Select with Condition
```sql
SELECT * FROM PERSON WHERE ID = 103;
```

## 9. Delete Data from Table
```sql
DELETE FROM PERSON WHERE ID = 103;
```

## 10. Inserted Data (Tabular Form)
| ID  | NAME         | CITY    |
|-----|-------------|---------|
| 101 | SUBHADIP    | KOLKATA |
| 104 | RAHUL SHARMA | MUMBAI  |
| 105 | AMIT KUMAR  | PUNE    |
| 106 | VIKAS SINGH | CHENNAI |