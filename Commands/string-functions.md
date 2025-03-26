# String Functions in PostgreSQL

PostgreSQL provides various string functions for text manipulation. Below are commonly used string functions with examples using the `employee` table.

## 1. CONCAT() - Concatenate Strings
Used to combine multiple strings into one.
```sql
SELECT CONCAT(ename, ' - ', department) AS employee_info FROM employee;
```

## 2. CONCAT_WS() - Concatenate with Separator
Allows specifying a separator between concatenated values.
```sql
SELECT CONCAT_WS(', ', ename, city, department) AS employee_details FROM employee;
```

## 3. SUBSTR() - Extract Substring
Extracts a part of a string starting from a given position.
```sql
SELECT SUBSTR(email, 1, 5) AS email_prefix FROM employee;
```

## 4. LEFT() and RIGHT() - Get Left/Right Substring
Extracts a certain number of characters from the left or right of a string.
```sql
SELECT LEFT(ename, 3) AS name_start FROM employee;
SELECT RIGHT(email, 10) AS email_domain FROM employee;
```

## 5. LENGTH() - Get String Length
Returns the number of characters in a string.
```sql
SELECT ename, LENGTH(ename) AS name_length FROM employee;
```

## 6. UPPER() and LOWER() - Convert Case
Converts text to uppercase or lowercase.
```sql
SELECT UPPER(ename) AS name_upper, LOWER(city) AS city_lower FROM employee;
```

## 7. TRIM(), LTRIM(), RTRIM() - Remove Spaces
Removes spaces from a string.
```sql
SELECT TRIM('   PostgreSQL   ') AS trimmed_text;
SELECT LTRIM('   Left Trim') AS left_trimmed;
SELECT RTRIM('Right Trim   ') AS right_trimmed;
```

## 8. REPLACE() - Replace Substring
Replaces occurrences of a substring within a string.
```sql
SELECT REPLACE(email, '@email.com', '@company.com') AS updated_email FROM employee;
```

## 9. POSITION() - Find Substring Position
Finds the position of a substring within a string.
```sql
SELECT POSITION('@' IN email) AS at_position FROM employee;
```

## 10. STRING_AGG() - Aggregate Strings
Concatenates multiple rows into a single string with a separator.
```sql
SELECT STRING_AGG(ename, ', ') AS employee_names FROM employee;
```

