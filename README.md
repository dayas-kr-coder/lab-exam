# Database queries using MySQL

```
1. Create a table Student with the following fields and insert at  least 5 records into the table except for the column Total.

  Roll_Number 		Integer 		Primary key
  Name		        Varchar(25)
  Batch           Varchar(15)
  Mark1 		 	    Integer
  Mark2			      Integer
  Mark3			      Integer
  Total 			    Integer

a. List the details of students in Commerce batch.
b. Display the name and total marks of students who are failed (Total < 90).
c. Display the name of students in alphabetical order and in batch based.
```

## <center>ANSWERS</center>

```sql
-- (1.) Create the Student table
CREATE TABLE Student (
  Roll_Number INT PRIMARY KEY,
  Name VARCHAR(25) NOT NULL,
  Batch VARCHAR(15) NOT NULL,
  Mark1 INT NOT NULL,
  Mark2 INT NOT NULL,
  Mark3 INT NOT NULL,
  Total INT
);
```

```sql
-- (1.) Insert 5 records into the Student table
INSERT INTO Student (Roll_Number, Name, Batch, Mark1, Mark2, Mark3) VALUES
  (1001, 'Rohit', 'Computer', 80, 80, 80),
  (1002, 'Aruns', 'Biology', 20, 25, 30),
  (1003, 'Gayathri', 'Computer', 70, 78, 80),
  (1004, 'Vishnu', 'Biology', 10, 30, 40),
  (1005, 'Rahul', 'Commerce', 80, 79, 60);
```

```sql
-- a. List the details of students in Commerce batch.
UPDATE Student
Total = Mark1 + Mark2 + Mark3;
```

```sql
-- b. Display the name and total marks of students who are failed (Total < 90).
UPDATE Student
Total = Mark1 + Mark2 + Mark3;
```

```sql
-- c. Display the name of students in alphabetical order and in batch based.
SELECT Name FROM Student
ORDER BY Name;
```
