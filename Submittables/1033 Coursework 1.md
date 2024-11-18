# Chloe Loveland 1033 Coursework 1

## Task 1
![[coursework1ERdiagram.png|centre|375]]

## Task 2
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

## Task 3
### Part a
```
SELECT MAX(email)
FROM operator
ORDER BY email;
```
Returns:
![[Pasted image 20241113000512.png|left|300]]

### Part b
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
### Part c
```
SELECT COUNT(*) AS "Number of Stops", Name 
FROM district 
JOIN busstop ON district.name = busstop.district 
GROUP BY Name
HAVING COUNT(*) > 4;
```

Returns:
![[Pasted image 20241113002233.png|left|300]]

### Part d
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

## Task 4
