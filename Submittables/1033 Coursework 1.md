# Chloe Loveland 1033 Coursework 1

## Task 1
![[coursework1ERdiagram.png|left|400]]

## Task 2
**Commands entered:**
```
CREATE TABLE District(
	Name VARCHAR(30) NOT NULL,
	OfficePhone CHAR(13),
	PRIMARY KEY(Name)
);
```
- Phone is intended to be stored as a number with a country code i.e. +447000000000
- Name is the primary key as this is stated to be unique

```
CREATE TABLE BusStop(
	ID int NOT NULL,
	District VARCHAR(30),
	Description VARCHAR(30),
	PRIMARY KEY(ID),
	FOREIGN KEY (District) REFERENCES District(Name)
);
```
- The foreign key represents the many to one relationship between BusStop and District

```
CREATE TABLE Route(
	RouteNumber int NOT NULL,
	Frequency int,
	Start int,
	Destination int,
	PRIMARY KEY(RouteNumber),
	FOREIGN KEY(Start) REFERENCES BusStop(ID),
	FOREIGN KEY(Destination) REFERENCES BusStop(ID)
);
```
- Frequency must be a float as it is the number of buses per hour (this could be less than one)
- Route has a 2-Many relationship via the two foreign key references to BusStop(ID)

```
CREATE TABLE Operator(
	Name VARCHAR(30),
	Telephone CHAR()
);
```