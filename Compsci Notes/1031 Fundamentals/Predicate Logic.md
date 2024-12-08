Predicate logic is an extension of [[propositional logic]] which allows for reasoning over infinite sets of values.

## Predicates
A predicate is essentially a proposition with a piece of information missing. The predicate P(x) becomes a proposition - and thus is true or false - when we instantiate its variables with values.

> [!Example]
> - For example, a predicate may look like "even(x) = number x is even"
> - this predicate becomes a proposition when we add a value, like even(6)
> 	- This has a truth value, where even(x) did not

<br>

## Universal quantifier
- Need to capture that variable x **holds a property over all of the values** of a set.
- This is done using the **universal quantifier** ($\forall$).
	- Usage:
	- $\forall x \in A$ means "for all values in set A"
	-  $\forall x \in A \  \&\  P(x)$ means "for all values in set A, P(x) holds"
		- The $\&$ symbol is **simply a spacer**, it has <mark class="hltr-blue">no logical meaning</mark>.

> [!Info] Proving an universally quantified formula true or false
>1. To show formula is <mark class="hltr-green">true</mark>, you must show that for each element that P(x) is true.
>2. To show formula is <mark class="hltr-red">false</mark>, you must only show one **witness value** where P(x) is false.

<br>

## Existential Quantifier
- Where universal quantifier is AND applied over a whole set, existential quantifier applies OR over a whole set.
- Usage:
	- $\exists x \in A\ \&\  (even(x) \land prime(x))$ means *at least one* in set $A$ is even and prime.

> [!Info] Proving an existentially quantified formula true or false
> 1. To show formula is <mark class="hltr-green">true</mark>, you must only show one **witness value** where P(x) is true.
> 2. To show formula is <mark class="hltr-red">false</mark>, you must show that for each element that P(x) is false.

<br>

## Relationship between $\forall$ and $\exists$
- $\forall x \in S \ \& \ P(x) \equiv ¬(\exists x \in S \ \& \ ¬P(x))$
- $\exists x \in S \ \& \ P(x) \equiv ¬(\forall x \in S \ \& \ ¬P(x))$
- it's a bit like [[laws of equivalence|De Morgan's law]] but it's not called that


## Combining $\forall$ and $\exists$