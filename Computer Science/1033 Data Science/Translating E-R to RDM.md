Translating [[Entity-Relationship diagram]] to the [[Relational Data model]] involves many rules

- To convert an [[Entity-Relationship diagram]] to a [[Relational Data model|relational database]] we translate all strong [[entity]] sets to a [[relation (table)]]
	- So all the rectangles pretty much
	- the ovals (attributes) will be fields in the relation
- Many-to-many relationships need to be represented by their own table
	- They should not just be a relationship
- When translating a [[relationship]] set with no key, attributes must include
	- Keys for each participating [[entity]] set (as [[Foreign Key|foreign keys]])
	- All descriptive attributes of the relationship set
## Translating relationship sets with [[Participation Constraint|key constraints]]
- If some entities can only participate once in a relationship, we can make the entity an attribute of the entity it is related to
	- Example: if each department has one manager, we do not need a [[Relation (table)|table]] for manager
	- We can just make Dept_manager an attribute of department
## Translating [[weak entity]] sets
- the weak entity set and identifying relationship set are translated into a single table
## Translating class [[Hierarchy]]
![[ISAheirarchy.png|500]]
- Map each of the entity sets Employees, Hourly-Emps, Contract-Emps to a distinct relation
- **OR**
- Create only 2 relations ![[Pasted image 20241015110116.png|left|400]]
## Translating E-R diagrams with [[aggregation]]
- [[!TODO]]