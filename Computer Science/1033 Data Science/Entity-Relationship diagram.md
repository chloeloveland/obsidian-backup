---
tags:
  - 1033-Data-Sci
---
- A form of conceptual data model which models data and constraints as [[Entity]] and [[Relationship]]
- [[Entity]] are represented by rectangles
- attributes by ovals
- [[Relationship]] by diamonds - their many or one is written at the bases of the line (see diagram)

> [!diagram] Example of an E-R diagram of a bike shop
> ![[entityRelationshipBikeShop.png|400]]
## [[Entity]] vs attribute
- Should address be an attribute of employees or an entity connected to employees?
	- if we have several addresses per employee, address **must** be modelled as an entity
	- if the **structure** is important, address **must** be modelled as an entity.