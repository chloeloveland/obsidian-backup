---
tags:
  - 1031-Fundamental
---
## Unary Relations
- Unary relations are a way to identify elements in a set which have an important property.
	- They return true or false
- fundamentally, a relation is an application of [[subset|subsets]]
	
>[!example]
>- performing primary(red) on aan [[Element]] set of **colours** would return true.
>- performing even(1) on an element of set **numbers** would return false.
	
### Defining
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

- Binary relations define relations between values in two sets
- for example, if set P is people and set A is pets, we can define the relation as **has**
- then we can ask if person **has** pet
- **has** is thus a [[subset]] of the [[cartesian product]] $A\times P$
- Binary relations can be visualised as **directed graphs** where the arrow points from the first in the [[Tuples|tuple]] to the second.

## Relations
- Relations can have [[Properties of relations|properties]].