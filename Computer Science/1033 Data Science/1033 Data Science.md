[[Databases]]
[[Data abstractions]]

## Data Independence

- there are two levels of data independence
- **Logical independence** is the idea that changes to the conceptual schema should not require changes to the external schema, or rewrites of the application
- **Physical independence**  is the idea that changes to the internal schema (i.e hardware changes or different filesystem) should not require any change to the conceptual or external schemas

---

# Database design




## Keys

- Every entry in a database needs a key field.
- The key is a field which has a unique value for every entry.
- For example, a bank account has an account number, and a student has a student ID number
- A key can actually consist of multiple combined attributes
- this is a superkey; any set of attributes which can identify an entity
- For example, all houses must have a unique address. While the house number and postcode are not individually unique, the combination of postcode and house number is
- A primary key is the key chosen to serve as the key for the entity set

## Relationships

- A relationship is an association among several entities
- in an E-R diagram, a relationship can optionally have attributes to describe them
- Relationships can take different forms: 1-1, 1-many, many-1, many-many

## Participation Constraint

- A **participation constraint** imposes some requirements on the number of times an entity participates in a relationship
    - Total participation: Each entity must participate in at least one relationship
        - every order to an online store **must have a customer**
    - Partial participation: an entity may not participate in a relationship
        - not all library card holders will borrow a book
        - not all books will be borrowed
        - so we can't have total participation

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

