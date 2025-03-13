# Data Types in PostgreSQL

PostgreSQL provides a rich set of data types to handle different kinds of data efficiently.

## 1. Numeric Data Types
Used for storing numbers.

| Data Type  | Description |
|------------|------------|
| `SMALLINT` | Stores integers from -32,768 to 32,767 |
| `INTEGER`  | Stores integers from -2,147,483,648 to 2,147,483,647 |
| `BIGINT`   | Stores very large integers |
| `DECIMAL(p,s)` | Stores fixed-point numbers with precision `p` and scale `s` |
| `NUMERIC(p,s)` | Similar to `DECIMAL`, stores exact numeric values |
| `REAL`     | Floating-point number with 6 decimal places of precision |
| `DOUBLE PRECISION` | Floating-point number with 15 decimal places of precision |

## 2. Character Data Types
Used for storing text.

| Data Type  | Description |
|------------|------------|
| `CHAR(n)`  | Fixed-length string of `n` characters |
| `VARCHAR(n)` | Variable-length string with a maximum length of `n` |
| `TEXT`     | Stores an unlimited-length string |

## 3. Date and Time Data Types
Used for handling date and time values.

| Data Type  | Description |
|------------|------------|
| `DATE`     | Stores a calendar date (YYYY-MM-DD) |
| `TIME`     | Stores time of day (HH:MI:SS) |
| `TIMESTAMP` | Stores date and time (YYYY-MM-DD HH:MI:SS) |
| `TIMESTAMPTZ` | Stores timestamp with timezone information |
| `INTERVAL` | Stores a time interval (e.g., '1 year 2 months') |

## 4. Boolean Data Type
Used for storing `TRUE` or `FALSE` values.
```sql
CREATE TABLE USERS (
    UserID SERIAL PRIMARY KEY,
    IsActive BOOLEAN DEFAULT TRUE
);
```

## 5. JSON Data Types
Used for storing JSON-formatted data.

| Data Type  | Description |
|------------|------------|
| `JSON`     | Stores JSON data but does not enforce structure |
| `JSONB`    | Stores JSON in a binary format with indexing support |

## 6. Array Data Type
Used for storing arrays.
```sql
CREATE TABLE STUDENTS (
    StudentID SERIAL PRIMARY KEY,
    Subjects TEXT[]
);
```

## 7. UUID (Universally Unique Identifier)
Used for storing unique identifiers.
```sql
CREATE TABLE DEVICES (
    DeviceID UUID DEFAULT gen_random_uuid() PRIMARY KEY
);
```

## 8. Special Data Types
| Data Type  | Description |
|------------|------------|
| `BYTEA`    | Stores binary data (e.g., images, files) |
| `CIDR`     | Stores IPv4 or IPv6 network addresses |
| `INET`     | Stores individual IP addresses |
| `MACADDR`  | Stores MAC addresses |

These data types allow PostgreSQL to efficiently store and manage different types of information in a structured way.

