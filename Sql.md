# SQL Basics

## 1. Introduction to SQL
SQL (Structured Query Language) is used to manage and manipulate relational databases. It allows users to create, retrieve, update, and delete data efficiently.

### Types of SQL Commands
- **DDL (Data Definition Language)** – Defines database structure (`CREATE`, `ALTER`, `DROP`, `TRUNCATE`)
- **DML (Data Manipulation Language)** – Manages data (`INSERT`, `UPDATE`, `DELETE`)
- **DQL (Data Query Language)** – Queries data (`SELECT`)
- **DCL (Data Control Language)** – Controls access (`GRANT`, `REVOKE`)
- **TCL (Transaction Control Language)** – Manages transactions (`COMMIT`, `ROLLBACK`, `SAVEPOINT`)

---

## 2. SQL Data Types
### Numeric Types:
- `INT`, `FLOAT`, `DECIMAL`

### String Types:
- `VARCHAR`, `TEXT`, `CHAR`

### Date & Time:
- `DATE`, `TIME`, `TIMESTAMP`

---

## 3. SQL Commands
### DDL Commands:
```sql
CREATE TABLE students (
    id INT PRIMARY KEY,
    name VARCHAR(100),
    age INT
);
ALTER TABLE students ADD COLUMN email VARCHAR(100);
DROP TABLE students;
TRUNCATE TABLE students;
```

### DML Commands:
```sql
INSERT INTO students (id, name, age) VALUES (1, 'John Doe', 22);
UPDATE students SET age = 23 WHERE id = 1;
DELETE FROM students WHERE id = 1;
```

### DQL Command:
```sql
SELECT * FROM students WHERE age > 20 ORDER BY name;
```

### DCL Commands:
```sql
GRANT SELECT ON students TO user_name;
REVOKE SELECT ON students FROM user_name;
```

### TCL Commands:
```sql
COMMIT;
ROLLBACK;
SAVEPOINT save1;
```

---

## 4. SQL Clauses
- **WHERE** – Filters records
- **GROUP BY** – Groups data
- **HAVING** – Filters grouped data
- **ORDER BY** – Sorts records

Example:
```sql
SELECT age, COUNT(*) FROM students GROUP BY age HAVING COUNT(*) > 1 ORDER BY age DESC;
```

---

## 5. SQL Joins
- **INNER JOIN** – Matches records in both tables
- **LEFT JOIN** – All records from the left table + matching records from the right table
- **RIGHT JOIN** – All records from the right table + matching records from the left table
- **FULL JOIN** – All records from both tables

Example:
```sql
SELECT students.name, courses.course_name FROM students
INNER JOIN courses ON students.id = courses.student_id;
```

---

## 6. SQL Constraints
- **PRIMARY KEY** – Uniquely identifies each record
- **FOREIGN KEY** – Maintains relationships between tables
- **NOT NULL** – Ensures a column cannot have NULL values
- **UNIQUE** – Ensures unique values in a column
- **CHECK** – Defines a condition for values

Example:
```sql
CREATE TABLE orders (
    order_id INT PRIMARY KEY,
    customer_id INT,
    order_date DATE,
    FOREIGN KEY (customer_id) REFERENCES customers(id)
);
```

---

## 7. SQL Functions
### Aggregate Functions:
```sql
SELECT COUNT(*) FROM students;
SELECT AVG(age) FROM students;
```
### String Functions:
```sql
SELECT UPPER(name) FROM students;
SELECT LENGTH(name) FROM students;
```
### Date Functions:
```sql
SELECT CURDATE();
SELECT DATEDIFF('2025-12-31', '2025-01-01');
```

---

## 8. Subqueries and Views
### Subquery Example:
```sql
SELECT name FROM students WHERE age = (SELECT MAX(age) FROM students);
```
### View Example:
```sql
CREATE VIEW student_view AS SELECT name, age FROM students;
```

---

## 9. Indexes
Indexes improve search performance.
```sql
CREATE INDEX idx_student_name ON students(name);
```

---

## 10. Stored Procedures & Triggers
### Stored Procedure:
```sql
DELIMITER //
CREATE PROCEDURE GetStudents()
BEGIN
    SELECT * FROM students;
END //
DELIMITER ;
```
### Trigger:
```sql
CREATE TRIGGER before_student_insert
BEFORE INSERT ON students
FOR EACH ROW
SET NEW.name = UPPER(NEW.name);
```

---

## Conclusion
SQL is a powerful language for managing databases, offering a wide range of functionalities to store, retrieve, and manipulate data efficiently. Mastering SQL fundamentals helps in working with relational databases effectively!
