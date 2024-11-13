---
tags:
  - 1031-Fundamental
---
## Unary Relations
- Unary relations are a way to identify elements in a set which have an important property.
	- They return true or false
- fundamentally, a relation is an application of [[Subset|subsets]]
	
>[!example]
>- performing primary(red) on an [[Element]] set of **colours** would return true.
>- performing even(1) on an element of set **numbers** would return false.
	
### Defining Unary Relations
###### English
- We can use English i.e. primary(colours), primary(x) = true when x is in {red, green, yellow}
	- Pros: this is simple, easy to read and write
	- Cons: This is *not* concise at all, and can be ambiguous / up to interpretation
###### Listing
- To be less ambiguous (more mathematical), we would list the primary colours as a set
	- $primary= \{red, blue, yellow\}$
	- This could use listing (above), [[Expressing Sets#Set Comprehension|set comprehension]], or [[Expressing Sets#Recursion|recursion]]
	- Pros: very precise, no ambiguity
	- Cons: difficult to write, you need to know the notation to interpret
		- **overall better**
## Binary relations
- Binary relations define relations between values in *two* sets
- a binary relation is a [[Subset]] of the [[Cartesian Product]] $A\times P$
###### English Definition
- for example, if set P is people and set A is pets, we can define the relation as **has**
- then we can ask if person **has** pet
###### Recursive definition
- Binary relations can be defined [[Expressing Sets#Recursion|recursively]]

> [!example]
> Base case: $(0, 1)\in less$
> Recursive case: $if (x,y)\in le$$ss$ then $(x,y+1)\in less$ and $(x+1,y+1)\in less$ 
> ![[recursive binary relation]]
## Binary relations as Graphs
- Binary relations can be visualised as **directed graphs** where the arrow points from the first in the [[Tuples|tuple]] to the second.
	- These are generated through a simple process
		1. Every element of set A is a node
		2. For each pair $(x,y)\in \Bbb R$ add an edge (arrow) x->y
- With a graph like this, we can ask if a statement holds by checking if there is an edge between the two elements
- we can also check if [[Properties of relations]] hold
## Properties
- Relations can have [[Properties of relations|properties]].
### Functions
- One application of relations is [[Function|functions]].
	- Note: every function is a relation but not every relation is a function.