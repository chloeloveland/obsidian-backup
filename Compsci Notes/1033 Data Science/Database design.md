---
tags:
  - 1033-Data-Sci
---
- Database design can be divided into six steps
    1. **Requirements analysis** - what data; for what application; what operations are most frequent
    2. **Conceptual design** - A high level description of the data to be saved and the constraints put on the design - this step usually involves the creation of an [[Entity-Relationship diagram]] OR [[Normalisation]]
    3. **Logical design** - decide upon a DBMS; convert the conceptual design into the database [[Schema]] in the chosen DBMS
    4. **Schema Refinement** - analyse the collection of relations; identify potential problems; refine the [[Schema]]
    5. **Physical design** - ensure that the design meets performance requirements; build indexes, cluster tables etc; redesign parts of the database [[Schema]]
    6. **Application and security design** - write the application; identify data that can be accessible by certain users; take steps to ensure that access rules are correctly enforced
