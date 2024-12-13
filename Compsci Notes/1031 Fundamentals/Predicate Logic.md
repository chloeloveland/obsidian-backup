Predicate logic is an extension of [[propositional logic]] which allows for reasoning over large and infinite sets of values.

## Predicates
A predicate is essentially a [[Propositional Logic|proposition]] with a piece of information missing. The predicate P(x) becomes a proposition - and thus is true or false - when we instantiate its variables with values.

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
<br>

## Combining $\forall$ and $\exists$
The existential and universal quantifiers can be combined in the same predicate formula. When combined, the statements should simply be read left to right. See below:
$$
\forall x \in \{2,...,4\} \ \& \ \exists y \in \{1,...,5\}\ \& \ (x>y)
$$
This statement should be read as:
"**For every value** in {2,...,4} there **exists** a value in {1,...,5} which is less than it"

Note that the order of operation (left to right) only matters when combining *different* quantifiers. But for ease of use just do it always.


> [!Info] Proving true or false when combining $\forall$ and $\exists$
> - Take the above example $\forall x \in \{2,...,4\} \ \& \ \exists y \in \{1,...,5\}\ \& \ (x>y)$
> - Simply apply the existing rules for these operators when in isolation
> - So to show it is <mark class="hltr-green">true</mark>, we need to show that for **every value** in {2,...,4} there is at least one **witness value** in {1,...,5} where x>y
> - Or to show <mark class="hltr-red">false</mark>, we need to show that there is at least one **witness value** in {2,...,4} where **every value**  in {1,...,5} means it is false.
> - ***This is a lot more intuitive than it looks***