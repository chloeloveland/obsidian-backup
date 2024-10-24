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

## *Ordering*
- Results can be ordered using the `ORDER BY` statement
- e.g. `ORDER BY S.rating`

## [[sets|Set]]-manipulation constructs
- `UNION` $\cup$
- `INTERSECT` $\cap$
- `EXCEPT` -
- By default, duplicates are not shown
- to show, use `X ALL` (e.g. `UNION ALL`)
- **Not supported by MySQL**

## Nested SQL
- SQL statements can be nested in one another

> [!Example]
> ![[Pasted image 20241022104046.png|500]]

## Aggregate operators

- SQL supports five aggregate operations, which can be applied on any column of a relation
	- `COUNT([DISTINCT]A)` 
		- The number of (unique) values in A
	- `SUM(A)`
		- The sum of values in A
	- `AVG(A)`
		- The average of all values in A
	- `MAX(A)`
		- The max value in A
	- `MIN(A)`
		- The min value in A
- All can use the `DISTINCT` keyword, in `COUNT` as example

> [!Warning] 
> If `SELECT` uses an aggregate operation, then it must use *only* aggregate operations, unless the query contains a `GROUP BY` clause, MySQL would return an arbitrary answer.

>[!Tip]
> - Aggregate operations **cannot be nested**
> 	- instead of `MIN(AVG())`, something like:
> ```SELECT MIN (avAge)  
FROM (SELECT S.rating, AVG (S.age) AS avAge  
FROM Sailors S  
GROUP BY S.rating) AS minAge```
```

## *Group by* and *Having*
- `GROUP BY` groups rows that have the same values into summary rows.
- `HAVING` is similar to the `WHERE` clause but is compatible with aggregate statements.

> [!Info] General form of extended SQL
> ```
> SELECT target-list
> FROM relation-list
> WHERE qualification
> GROUP BY grouping-list
> HAVING group-qualification
>```

