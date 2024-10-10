---
tags:
  - 1033-Data-Sci
---
- SQL (Structured query language) is a [[Relational Data model|relational query language]]
- it is not case sensitive
- A query looks like this
## Choosing data
```
SELECT *
FROM Students
WHERE S.age=18
```
- This query would select all (asterisk is wildcard) records from students where the age is 18
## Making/deleting tables
- Tables are created via the CREATE TABLE command:
```
CREATE TABLE Students
	(sid CHAR(20)
	age INTEGER
	mark DECIMAL(5,2))
```
- Tables are deleted via the DROP TABLE command // this is scary, and is a big part of [[SQL injection]]
## Changing Data
- Data can be inserted using the `INSERT INTO tableName VALUES(value, value)` command
- Data can be modified using the `UPDATE tableName SET fieldName = value`
	- We can use WHERE statements with these too
## Foreign keys
