---
tags:
  - 1031-Fundamental
---
In some important systems (car self drive, plane **autopilot**, nuclear reactor etc.) it is critical that software never fails. In these situations, mere testing is not enough:

> "Testing can show presence of errors but not their absence" - Dijkstra

So instead we use mathematical reasoning (proof) to rigorously show that a property holds.

- A proof is a structured mathematical argument which rigorously explains why a [[theorem]] is true.
- A proof shows why the conclusion must hold given the assumptions in the theorem.
- Normally based on using **deduction steps**: using known facts and definitions to **infer** a new fact.

## Direct proof
- A direct proof is a basic type of proof underlying most proof techniques.
- Consists of a series of **deduction steps** that link together to show directly why the conclusion stated in the [[theorem]] follows from the given assumptions.
- Each deduction step states what it is using and what new fact is derived

> [!Example] Example of what a deduction step looks like
> By assumption $A\backslash B\neq \{\}$ and definition of set difference we know that $A$ contains some values which are not in $B$ 

- Sometimes a direct proof is not possible because we do not have enough information.
- So we can use proof techniques such as **proof by cases**.

## Proof by cases
- Split proof into a number of **cases**
- Each case has a new **assumption**
- Give a proof for each case using extra **assumption**

## Counter example
- It can be shown that a [[theorem]] does not hold by using a **counter example**
- for a theorem to be true, when its assumptions are true its conclusion must **always** be true
- if we can give an example where conclusion is **not** true, then the theorem is false.

## Proof by induction
- A proof technique used to prove theorems over [[Recursive Function Definition|recursively]] defined sets of values.

> [!info] Consider using **proof by induction** for theorems of this form:
> - [[Theorem]]: For all natural numbers $n\in \Bbb N$ we have property $P(n)$

 - Property $P(n)$ can be any [[Boolean logic|boolean]] property involving [[Common Sets|natural number]] n that you want to show holds.

> [!Example] Examples of this:
> - <mark class="hltr-green">$P(n)$ is $n\times (5+3) = (n\times 5) + (n\times 3)$</mark>
> - <mark class="hltr-green">$P(n)$ is $(2^n + 2) > n^2$</mark>
>- <mark class="hltr-red">$P(n)$ is $(n^2 + 5)\times 2$</mark> **This is not one, must be an equation**


> [!Diagram] Proof by induction template
> 1. **Induction Base**: Let $n=0$. Show $P(0)$ holds.
> 2. **Induction Step:**