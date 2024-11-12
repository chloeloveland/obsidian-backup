# Chloe Loveland 1033 Coursework 1

## Task 1
![[coursework1ERdiagram.png|left|400]]

## Task 2
Commands entered:
```
CREATE TABLE District(
	Name VARCHAR(30) NOT NULL,
	OfficePhone VARCHAR(13),
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