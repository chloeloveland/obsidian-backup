---
tags:
  - 1031-Fundamental
---
Propositional logic is a simple logic used for reasoning about expressions that are either **true** or **false**. This is important in computing where many things exist in a binary state.

## Syntax
- Propositional variables are represented by letters
	- Typically $p, q, r...$

| Informal | Mathematical | Circuits      |
| :------- | :----------- | ------------- |
| True     | T            | 0             |
| False    | F            | 1             |
| not p    | $¬p$         | $\bar p$      |
| p or q   | $p\lor q$    | $p+q$         |
| p and q  | $p \land q$  | $p \bullet q$ |

## Semantics
- Each **proposition** has the value T or F
- not is a.k.a. **negation**
- or is a.k.a. **disjunction**
- and is a.k.a. **conjunction**

## Truth tables
We can use truth tables to check all the possible behaviours of a propositional formula.

> [!Example] 
> 
| p   | q   | $q \land ¬p$ | $p\land (q\land ¬p)$ |
| --- | --- | ------------ | -------------------- |
| F   | F   | F            | F                    |
| F   | T   | T            | T                    |
| T   | F   | F            | T                    |
| T   | T   | F            | T                 |

## Satisfiability
A formula is **satisfiable** if any combination of values will make it true.

Checking for satisfiability can be difficult when there are lots of propositions.
The size of the truth table doubles with each additional one (exponential growth).

**SAT solver** algorithms check for satisfiability for you.

## Tautology + Contradiction
A **tautology** is a propositional formula that <mark class="hltr-green">always evaluates to **true**</mark>.
A **contradiction** is a propositional formula that <mark class="hltr-red">always evaluates to **false**.</mark>

## Logical equivalence
When two **propositional formulae** have the same truth table, they are **logically equivalent**.
This is the basis of the **[[Laws of Equivalence]].**

## Implication
- Implication is another logical connective, like $\land$ and $\lor$
- Looks like: $p\implies r$
- Means "If $p$ is true then $r$ is true"

| p   | r   | $p\implies r$ |
| --- | --- | ------------- |
| F   | F   | T             |
| F   | T   | T             |
| T   | F   | F             |
| T   | T   | T             |


## Limitations
Propositional logic cannot reason about properties over infinite sets.
To do this, we use [[Predicate Logic]], an extension of propositional logic.

---
## See also:
- [[Boolean logic]]