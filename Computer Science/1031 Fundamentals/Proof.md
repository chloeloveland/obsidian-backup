In some important systems (car self drive, plane **autopilot**, nuclear reactor etc.) it is critical that software never fails. In these situations, mere testing is not enough:

> "Testing can show presence of errors but not their absence" - Dijkstra

So instead we use mathematical reasoning (proof) to rigorously show that a property holds.

- A proof is a structure mathematical argument which rigorously explains why a [[theorem]] is true.
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
