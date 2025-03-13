# SQL Clauses in PostgreSQL

Clauses in PostgreSQL are used to filter, sort, and limit the data retrieved from a table.

## 1. WHERE Clause
Used to filter records based on a condition.
```sql
SELECT * FROM EMPLOYEE WHERE Salary > 50000;
```

## 2. DISTINCT Clause
Retrieves unique values from a column.
```sql
SELECT DISTINCT City FROM EMPLOYEE;
```

## 3. ORDER BY Clause
Sorts the result set in ascending (`ASC`) or descending (`DESC`) order.
```sql
SELECT * FROM EMPLOYEE ORDER BY Salary DESC;
```

## 4. LIMIT Clause
Limits the number of rows returned.
```sql
SELECT * FROM EMPLOYEE LIMIT 5;
```

## 5. LIKE Clause
Used to search for a pattern in a column.
```sql
SELECT * FROM EMPLOYEE WHERE Ename LIKE 'A%';
```
- `%` represents zero or more characters.
- `_` represents a single character.

## 6. IN / NOT IN Clause
Used to match a value in a list of values.
```sql
SELECT * FROM EMPLOYEE WHERE Eid IN (101, 103, 105);
SELECT * FROM EMPLOYEE WHERE Eid NOT IN (102, 104);
```

## 7. BETWEEN Clause
Filters data within a given range.
```sql
SELECT * FROM EMPLOYEE WHERE Salary BETWEEN 30000 AND 60000;
```

These clauses help in refining query results based on specific conditions and requirements.

