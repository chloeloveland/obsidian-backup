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
	Proportion TINYINT,
	PRIMARY KEY(Name),
	FOREIGN KEY(RouteNumber) REFERENCES Route(RouteNumber)
	);
```

