---
tags:
  - 1031-Fundamental
---
- A binary relation can have *properties*
- Let $R\subseteq A\times A$ where $A=\{1,2,3\}$:
##### Reflexive
- for every $x\in A$ must have $R(x,x)$
	- This means $(1,1), (2,2)$ etc. must be in $R$e
	- graph: check for self loops (where a node points to itself)
##### Symmetric
- whenever $R(x,y)$ holds then $R(y,x)$ must hold.
	- If we have $(1,2)$ we must have $(2,1)$
	- graph: check if edges are bi-directional
		- so <--> rather than -->
##### Transitive
- whenever $R(x,y)$ and $R(y,z)$ hold then $R(x,z)$ must hold (for any $x,y,x\in A$)
	- If $(2,3)\in A$ and $(3,1)\in A$, then $(2,1)\in A$
	- i.e. All linked steps can be done in one
	- ![[Properties of relations 2024-10-09 16.22.37.excalidraw]]
## Reasoning
- We can use the **properties** of [[Relations]] to deduce things about them.
- we can check if these relations hold using [[Relations#Binary relations as Graphs|graphs]]