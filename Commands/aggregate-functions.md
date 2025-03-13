# Aggregate Functions in PostgreSQL

Aggregate functions in PostgreSQL perform calculations on multiple rows and return a single value.

## 1. COUNT() - Count the Number of Rows
Returns the total number of rows in a table or satisfying a condition.
```sql
SELECT COUNT(*) FROM EMPLOYEE;
```
### Count with Condition
```sql
SELECT COUNT(*) FROM EMPLOYEE WHERE Salary > 50000;
```

## 2. SUM() - Sum of a Column
Calculates the total sum of a numeric column.
```sql
SELECT SUM(Salary) FROM EMPLOYEE;
```

## 3. AVG() - Average Value
Calculates the average value of a numeric column.
```sql
SELECT AVG(Salary) FROM EMPLOYEE;
```

## 4. MIN() - Minimum Value
Finds the smallest value in a column.
```sql
SELECT MIN(Salary) FROM EMPLOYEE;
```

## 5. MAX() - Maximum Value
Finds the largest value in a column.
```sql
SELECT MAX(Salary) FROM EMPLOYEE;
```

## 6. GROUP BY - Aggregate with Grouping
Groups data based on a column and applies aggregate functions.
```sql
SELECT DeptId, AVG(Salary) FROM EMPLOYEE GROUP BY DeptId;
```

## 7. HAVING - Filtering Aggregated Data
Used to filter results after applying `GROUP BY`.
```sql
SELECT DeptId, COUNT(*) FROM EMPLOYEE GROUP BY DeptId HAVING COUNT(*) > 5;
```

These aggregate functions help in performing statistical and analytical operations on PostgreSQL data.

