# Chloe Loveland 1033 Coursework 1

## Task 1
![[coursework1ERdiagram.png|left|400]]

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

> [!Warning] Changes made
> During data entry I realised that the relationship between operator and route is *not* many-one, and is instead many-many. I will add a join table for the relationship called `OperatorRoute` (this table will have a composite primary key). The diagram is updated to reflect this (see below), and the database will be updated.
> This involves deleting the existing foreign key constraints between operator and route and creating new ones.

![[coursework1ERdiagramupdated.png|left|400]]

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