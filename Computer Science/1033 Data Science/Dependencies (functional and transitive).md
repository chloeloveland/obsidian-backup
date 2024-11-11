---
tags:
  - 1033-Data-Sci
---
## Functional dependency
Definition: Attribute $B$ is functionally dependent upon attribute $A$ if a value of $A$ determines a single value of $B$ at any one time

Notation: *==$A\rightarrow B$==*  should be read as "$A$ determines $B$ " i.e. "$B$ is functionally dependent on $A$"
- Here $A$ is the ***==determinant==*** and $B$ is the ***==object of the determinant==***

### Partial Functional Dependency
- This is the situation that exists if it is necessary to only use a subset of the attributes of the composite determinant to identify its object uniquely.

## Transitive dependency
- Exists when there is an intermediate functional dependency
- if ==$A\rightarrow B$== and ==$B\rightarrow C$== then the transitive dependency *==$A\rightarrow B\rightarrow C$==* exists.