## Unary Relations
- Unary relations are a way to identify elements in a set which have an important property.
	- They return true or false
	- For example, performing primary(red) on a set of **colours** would return true.
	
#### Defining

- We can use English i.e. primary(colours)
- Or we can say primary is a [[subset]] of colours
- but to be less ambiguous, we would list the primary colours as a set
	- $primary= \{red, blue, yellow\}$
- a more mathematical way of writing primary(red) is to ask if red is an [[Element|member]] of colours
	- i.e. $red \in colours$?

## Binary relations

- Binary relations define relations between values in two sets
- for example, if set P is people and set A is pets, we can define the relation as **has**
- then we can ask if person **has** pet
- **has** is thus a [[subset]] of the [[cartesian product]] $A\times P$
- Binary relations can be visualised as **directed graphs** where the arrow points from the first in the [[Tuples|tuple]] to the second.
#### Properties
- A binary relation can have *properties*
- Let $R\subseteq A\times A$
	- Reflexive: for every $x\in A$ must have $R(x,x)$
		- This means 
	- Symmetric: Whenever $R(x,y)$ holds then $R(y,x)$ must hold.
	- Transitive: Whenever $R(x,y)$ and $R(y,z)$ hold then $R(x,z)$ must hold. (for any $x,y,x\in A$)