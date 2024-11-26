---
tags:
  - 1031-Fundamental
---
In some important systems (car self drive, plane **autopilot**, nuclear reactor etc.) it is critical that software never fails. In these situations, mere testing is not enough:

> "Testing can show presence of errors but not their absence" - Dijkstra

So instead we use mathematical reasoning (proof) to rigorously show that a property holds.

- A proof is a structured mathematical argument which rigorously explains why a [[Theorem]] is true.
- A proof shows why the conclusion must hold given the assumptions in the theorem.
- Normally based on using **deduction steps**: using known facts and definitions to **infer** a new fact.

## Direct proof
- A direct proof is a basic type of proof underlying most proof techniques.
- Consists of a series of **deduction steps** that link together to show directly why the conclusion stated in the [[Theorem]] follows from the given assumptions.
- Each deduction step states what it is using and what new fact is derived

> [!Example] Example of what a deduction step looks like
> By assumption $A\backslash B\neq \{\}$ and definition of set difference we know that $A$ contains some values which are not in $B$ 

- Sometimes a direct proof is not possible because we do not have enough information.
- So we can use proof techniques such as **proof by cases**.


> [!Tip] Direct proof equations can be chained together:
> 1. Know $a=b$
> 2. Know $b=c$
> 3. Know $c=d$
> 4. Know $d=e$
> 5. Thus, know $a=e$


## Proof by cases
- Split proof into a number of **cases**
- Each case has a new **assumption**
- Give a proof for each case using extra **assumption**
- Each case covers a possibility; all possibilities must have a case.

## Counter example
- It can be shown that a [[Theorem]] does not hold by using a **counter example**
- for a theorem to be true, when its assumptions are true its conclusion must **always** be true
- if we can give an example where conclusion is **not** true, then the theorem is false.

> [!Info] Template for counter example
> **Values:** {values go here}
> **Assumptions true:** {show the assumptions are true}
> **Conclusion false:** {show the conclusion is false}


## Proof by induction
- A proof technique used to prove theorems over [[Recursive Function|recursively]] defined sets of values.

> [!info] Consider using **proof by induction** for theorems of this form:
> - [[Theorem]]: For all natural numbers $n\in \Bbb N$ we have property $P(n)$

 - Property $P(n)$ can be any [[Boolean logic|boolean]] property (i.e. equation) involving the [[Common Sets|natural number]] n that you want to show holds.

> [!Diagram] Proof by induction template
> 1. Identify the property $P(n)$
> 	<mark class="hltr-orange">$P(n)$ is equation $triple(n)\over 3$ $=n$</mark>
> 1. **Induction Base:** Let $n=0$. Show $P(0)$ holds. (Direct proof)
> 2. **Induction Step:** Let $k\in \Bbb N$.
> 	Assume $P(k)$ holds (induction hypothesis)
> 	Then show $P(k+1)$ holds.
> > [!Info]
> By proving just the **base** and the **step**, we prove every step which leads from $k+1$

