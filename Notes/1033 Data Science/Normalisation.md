---
tags:
  - 1033-Data-Sci
---
- Normalisation is a mode of database design, not unlike [[Entity-Relationship diagram|Entity-Relationship diagrams]]
- Starts with one big [[Relation (table)|table]]
- Then a series of rules are applied to remove **anomalies**
	- Update anomaly
		- Occurs if a change to the value of a single attribute in a [[Relation (table)|table]] requires us to update *several rows* in the table.
	- Deletion anomaly
		- Occurs when deleting an [[Entity]] or [[Relationship]] causes us to lose information about a *different* entity or relationship.
	- Insertion anomaly
		- Occurs when we cannot add information about an [[Entity]] without adding information about some other entity which does not exist.
- There are several ***[[Normal Forms]]***, we cover the first three.

[[Dependencies (functional and transitive)]]