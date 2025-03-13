# Constraints in PostgreSQL

Constraints in PostgreSQL are rules enforced on data to maintain accuracy and integrity. Below are the commonly used constraints:

## 1. Primary Key Constraint
Ensures each row has a unique and non-null identifier.
```sql
CREATE TABLE EMPLOYEE (
    Eid INT PRIMARY KEY,
    Ename VARCHAR(50) NOT NULL
);
```

## 2. Not Null Constraint
Ensures a column cannot have NULL values.
```sql
CREATE TABLE EMPLOYEE (
    Eid INT PRIMARY KEY,
    Ename VARCHAR(50) NOT NULL
);
```

## 3. Unique Constraint
Ensures all values in a column are distinct.
```sql
CREATE TABLE EMPLOYEE (
    Eid INT PRIMARY KEY,
    Email VARCHAR(100) UNIQUE NOT NULL
);
```

## 4. Default Constraint
Assigns a default value if no value is provided.
```sql
CREATE TABLE EMPLOYEE (
    Eid INT PRIMARY KEY,
    Joining_Date DATE DEFAULT CURRENT_DATE
);
```

## 5. Check Constraint
Ensures values meet a specified condition.
```sql
CREATE TABLE EMPLOYEE (
    Eid INT PRIMARY KEY,
    Salary INT CHECK (Salary > 20000)
);
```

## 6. Foreign Key Constraint
Ensures referential integrity between two tables.
```sql
CREATE TABLE DEPARTMENT (
    DeptId INT PRIMARY KEY,
    DeptName VARCHAR(50)
);

CREATE TABLE EMPLOYEE (
    Eid INT PRIMARY KEY,
    DeptId INT,
    FOREIGN KEY (DeptId) REFERENCES DEPARTMENT(DeptId)
);
```

## 7. Serial (Auto Incrementing Integer)
Automatically increments an integer column.
```sql
CREATE TABLE EMPLOYEE (
    Eid SERIAL PRIMARY KEY,
    Ename VARCHAR(50)
);
```

