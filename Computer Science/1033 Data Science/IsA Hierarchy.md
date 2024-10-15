---
tags:
  - 1033-Data-Sci
---
- Sometimes it is natural to classify [[entity|entities]] into subclasses:

![{857B6BB1-F2EA-4287-9373-853FD2A00D96}.png|470](ISAheirarchy.png)

- Here the IsA is showing that both hourly employees and contract employees are employees
	- 
- Constraints:
    - Overlap constraints
        - Determine whether two subclasses are allowed to contain the same entity e.g can an employee be an Hourly_Emps as well as a Contract_Emps entity
    - Covering constraints
        - Determine whether the entities in the subclasses collectively include all entities in the superclass e.g does every employee entity also have to be an hourly_emps or contract_emps

>[!info] Reasons for using ISA
> - To add descriptive attributes specific to a subclass
> - To identify entities that participate in a relationship