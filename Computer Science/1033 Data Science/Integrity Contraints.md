---
tags:
  - 1033-Data-Sci
---
- An integrity constraint is a condition that must be true for any instance of the [[Databases|database]]
	- IC is specified when [[schema]] defined
	- IC is checked when [[relations]] modified
- When a relation satisfies all ICs it is *legal*
- A DBMS should disallow illegal instances
- Constraints can be *named* which allows the database to return the violated constraint to help fix the problem
	- If not named, the DB will just say "the primary key has been violated"

### [[Primary key]] constraint
- In [[SQL]] we can declare
	- A [[Key|key]] by the `UNIQUE` command
	- A primary key by the `PRIMARY KEY` constraint

## [[Foreign Key]] constraint
- If all foreign key constraints are enforced, referential integrity is achieved
- This constraint should be enforced by rejecting invalid entries (tuples with missing keys)