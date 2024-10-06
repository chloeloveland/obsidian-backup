[[Databases]]
[[Data abstractions]]


# Database design




## Keys



## Relationships



## Participation Constraint


## Weak Entities

- A weak entity is an entity with insufficient attributes to form a primary key
- they can be identifies uniquely by considering the primary key of another (owner) entity
    - Example:
        - Employees can purchase insurance policies to cover dependents
        - these dependents attributes are only *pname* and *dateofbirth*
        - this is a weak entity
        - so it is identified using the primary key of **employee**
- **Restrictions**
    - Owner and weak must have a one to many relationship (where owner is one)
    - Weak entity must have total participation in the identifying relationship

## Class Hierarchies

- Sometimes it is natural to classify entities into subclasses:

![{857B6BB1-F2EA-4287-9373-853FD2A00D96}.png|470](ISAheirarchy.png)

- Constraints:
    - Overlap constraints
        - Determine whether two subclasses are allowed to contain the same entity e.g can an employee be an Hourly_Emps as well as a Contract_Emps entity
    - Covering constraints
        - Determine whether the entities in the subclasses collectively include all entities in the superclass e.g does every employee entity also have to be an hourly_emps or contract_emps

