## Proofs
- Proof by cases: Split proof into several cases. Each case has its own assumption.
- Proof by induction:
	- Identify the property $P(n)$
	1. **Induction Base:** Let $n=0$. Show $P(0)$ holds. (Direct proof)
	2. **Induction Step:** Let $k\in \Bbb N$.
		- Assume $P(k)$ holds (induction hypothesis)
		- Then show $P(k+1)$ holds.

## Properties of relations
- Reflexive = each member has a relation where it points to itself i.e. $R(x,x)$
- Symmetric = if $R(2,1)$ then $R(1,2)$. Each relation has another which is flipped.
- Transitive = if $R(x,y)$ and $R(y,z)$, then $R(x,z)$. If a path exists, it can be done in one edge.

## Properties of functions
- A function must have **totality** (every input has an output) and **unambiguity** (always same out for a given in)
- Surjective: True if every value in the codomain is used.
- Injective: True if every input gives a unique output
- Bijective: True if both surjective and injective