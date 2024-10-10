- An integrity constraint is a condition that must be true for any instance of the [[Databases|database]]
	- IC is specified when [[schema]] defined
	- IC is checked when [[relations]] modified
- When a relation satisfies all ICs it is *legal*
- A DBMS should disallow illegal instances
- Constraints can be *named* which allows the database to return the violated constraint to help fix the problem
	- If not named, the DB will just say "the primary key has been violated"

### [[Keys#Primary Key|Primary key]] constraint
- In [[SQL]] we can declare
	- A [[keys|key]] by the `UNIQUE` command
	- A primary key by the `PRIMARY KEY` constraint

## Foreign Key
- A foreign key is a primary key in one relation that is used to refer to a tuple in another relations
	- can be one or more fields