---
tags:
  - 1033-Data-Sci
---
- SQL (Structured query language) is a [[Relational Data model|relational query language]]
- it allows us to query relational [[databases]]
- it is not case sensitive
# Data definition language (DDL)
## Making/deleting [[Relation (table)|tables]]
- Tables are created via the CREATE TABLE command:
```
CREATE TABLE Students
	(sid CHAR(20)
	age INTEGER
	mark DECIMAL(5,2))
```
- Tables are deleted via the DROP TABLE command // this is scary, and is a big part of [[SQL injection]]  
<br>
# Data manipulation language (DML)
## Changing Data
- Data can be inserted using the `INSERT INTO tableName VALUES(value, value)` command
- Data can be modified using the `UPDATE tableName SET fieldName = value`
	- We can use WHERE statements with these too
## Choosing data
```
SELECT *
FROM Students
WHERE S.age=18
```
- This query would select all (asterisk is wildcard) records from students where the age is 18

## Foreign keys
- [[Foreign key|Foreign keys]] are created using the `FOREIGN KEY (field) REFERENCES tableName` command
- Deletes and updates option should also be included as a part of the foreign key declaration
	- Default: `NO ACTION` 
		- reject delete/update
	- `CASCADE` 
		- delete all tuples that refer to deleted tuple
	- `SET NULL` / `SET DEFAULT` 
		- sets foreign key to value of referencing tuple
