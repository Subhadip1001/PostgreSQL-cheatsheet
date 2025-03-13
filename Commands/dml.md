# Data Manipulation Language (DML) Commands in PostgreSQL

## 1. Insert Data into a Table
```sql
INSERT INTO <TABLE_NAME> (column1, column2, ...) VALUES (value1, value2, ...);
```
### Example:
```sql
INSERT INTO EMPLOYEE (Eid, Ename, Email, Salary, Joining_Date)
VALUES (101, 'RAHUL SHARMA', 'rahul@example.com', 50000, '2024-01-15');
```

### Insert Multiple Rows
```sql
INSERT INTO EMPLOYEE (Eid, Ename, Email, Salary, Joining_Date) VALUES
(102, 'AMIT KUMAR', 'amit@example.com', 60000, '2023-11-20'),
(103, 'VIKAS SINGH', 'vikas@example.com', 55000, '2022-09-10');
```

## 2. Update Existing Data
```sql
UPDATE <TABLE_NAME>
SET column1 = new_value1, column2 = new_value2
WHERE condition;
```
### Example:
```sql
UPDATE EMPLOYEE
SET Salary = 70000
WHERE Eid = 101;
```

## 3. Delete Data from a Table
```sql
DELETE FROM <TABLE_NAME> WHERE condition;
```
### Example:
```sql
DELETE FROM EMPLOYEE WHERE Eid = 103;
```

## 4. Select Data from a Table
### Select All Columns
```sql
SELECT * FROM <TABLE_NAME>;
```
### Select Specific Columns
```sql
SELECT column1, column2 FROM <TABLE_NAME>;
```
### Select with Conditions
```sql
SELECT * FROM EMPLOYEE WHERE Salary > 50000;
```

## 5. Truncate Table (Delete All Data Without Dropping Table)
```sql
TRUNCATE TABLE <TABLE_NAME>;
```