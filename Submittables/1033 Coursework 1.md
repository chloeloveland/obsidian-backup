# Chloe Loveland 1033 Coursework 1

## Task i)
![[coursework1ERdiagram.png|centre|375]]

## Task ii)
```
CREATE TABLE District(
	Name VARCHAR(30) NOT NULL,
	OfficePhone CHAR(13),
	PRIMARY KEY(Name)
);
```

```
CREATE TABLE BusStop(
	ID int NOT NULL,
	District VARCHAR(30),
	Description VARCHAR(30),
	PRIMARY KEY(ID),
	FOREIGN KEY (District) REFERENCES District(Name)
);
```

```
CREATE TABLE Route(
	RouteNumber VARCHAR(4) NOT NULL,
	Frequency INT,
	Start INT,
	Destination INT,
	PRIMARY KEY(RouteNumber),
	FOREIGN KEY(Start) REFERENCES BusStop(ID),
	FOREIGN KEY(Destination) REFERENCES BusStop(ID)
);
```

```
CREATE TABLE Operator(
	Name VARCHAR(30),
	RouteNumber VARCHAR(4),
	Telephone CHAR(13),
	Email VARCHAR(40),
	Address VARCHAR(50),
	PRIMARY KEY(Name),
	FOREIGN KEY(RouteNumber) REFERENCES Route(RouteNumber)
);
```
---
> [!Warning] Changes made
> During data entry I realised that the relationship between operator and route is *not* many-one, but many-many. I will add a join table for the relationship called `OperatorRoute`. The diagram is updated to reflect this (see below), and the database will be updated.

![[coursework1ERdiagramupdated.png|centre|375]]

```
ALTER TABLE operator DROP INDEX operator_route_FK;
ALTER TABLE operator DROP COLUMN RouteNumber;
```

```
CREATE TABLE OperatorRoute(
	Name VARCHAR(30) NOT NULL,
	RouteNumber VARCHAR(4) NOT NULL,
	Proportion TINYINT DEFAULT 100,
	FOREIGN KEY(Name) REFERENCES Operator(Name),
	FOREIGN KEY(RouteNumber) REFERENCES Route(RouteNumber),
	PRIMARY KEY(Name, RouteNumber)
);
```

## Task iii)
### Part a)
```
SELECT MAX(email)
FROM operator
ORDER BY email;
```
Returns:
![[Pasted image 20241113000512.png|left|300]]

### Part b)
```
SELECT OfficePhone
FROM route 
JOIN busstop 
ON route.start = busstop.ID OR route.destination = busstop.ID 
JOIN district
ON busstop.district = district.name
WHERE routenumber = 22;
```

Returns:
![[Pasted image 20241113000620.png|left|175]]
The two phone numbers which need calling.
---
### Part c)
```
SELECT COUNT(*) AS "Number of Stops", Name 
FROM district 
JOIN busstop ON district.name = busstop.district 
GROUP BY Name
HAVING COUNT(*) > 4;
```

Returns:
![[Pasted image 20241113002233.png|left|300]]

### Part d)
```
SELECT DISTINCT email
FROM busstop
JOIN route ON route.start = busstop.ID OR route.destination = busstop.ID
JOIN operatorroute ON operatorroute.routenumber = route.routenumber
JOIN operator ON operatorroute.name = operator.name
WHERE description LIKE '%ESTATE%';
```

Returns:
![[Pasted image 20241113003325.png|left|300]]

All of the emails of bus operators that use the stop.

---
## Task iv)
1. {a} This approach seems like it would work. All the data is atomic, none of the tables have partial primary key dependencies, and no non-key fields rely on other non-key fields.
2. Does not work because non-key fields (staff name, staff phone number) depend on another non-key field (staff ID) - so does not meet third normal form.
3. Does not work because data is not atomic (i.e. all the info is stored in just 2 attributes) which means the solution does not meet first normal form.

## Task v)
1. {a} ...
	1. Performance data - could contain information that the query time is excessively long etc., which points to there being an underlying issue going on with the database.
	2. Query history - Could contain information on a user who is entering a high volume of queries, which could impact usability and speed for all other users.
2. ...
	1. Permission data - contains information on which users are allowed to do what - for security, users should ideally have the least possible permissions for what they need to do with the database, to ensure they cannot make any wrongful edits or deletions.
	2. Users data - if a user makes an unpermitted operation on the database, maliciously or otherwise, it may be important to know the user who is behind it.
	3. Connection data - similarly, if a user makes an unpermitted operation on the database it may be useful to know the source of the connection of the user which is responsible, as well as when they were connected etc.