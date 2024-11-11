---
tags:
  - 1033-Data-Sci
---
## First normal form (1NF)
- A [[Relation (table)|table]] is in first normal form if all data is ***==atomic==*** i.e. there are no multi-valued fields.

## Second normal form (2NF)
1. In **First Normal Form***
2. No non-[[key]] fields depend on a portion of the primary key
	- e.g. if a primary key is comprised of **two** fields and a field depends on only **one** of the primary fields, this is *not* in **2NF**

## Third Normal Form (3NF)
1. In **Second Normal Form**
2. no non-[[key]] fields depend on other non-key fields
	- i.e. each field in a record should contain information about the [[entity]] that is defined by the primary [[key]]