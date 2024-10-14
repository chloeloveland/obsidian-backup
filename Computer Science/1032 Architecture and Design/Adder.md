---
tags:
  - 1032-Archi
---
- An adder is a [[logical circuit]] which performs addition to binary numbers.
- It is used within the [[arithmetic logic unit]] and is essential for the functioning of the computer.
- It is made up of two *half adders*.

> [!Diagram] A half adder.
> ![[half-adder-circuit.png|300]]

> [!diagram] A full adder comprised of halves.
> ![[fullAdder.png|350]]

> [!info] Truth table of full adder
> ![[full-adder-truth-table.png|300]]

### Ripple carry vs Look ahead carry
- An adder for multiple bits must add together multiple full adders
- for example, an 8 bit adder must use 8 full adders
- in ripple carry, these adders feed their carry bits directly into the next full adder
- this is simple, but creates problems when considering [[propagation delay]]
	- this is because each adder must wait for the previous adder's carry bit
	- the adders operate sequentially which is slow
- to fix this, we can use look ahead carry.
- In a carry-lookahead, all the full adders operate simultaneously
- their outputs are combined using another [[logical circuit]] called the lookahead-carry unit