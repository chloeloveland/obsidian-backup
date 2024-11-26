---
tags:
  - 1032-Archi
---
- Propagation delay is a the time taken for a [[Logical circuit]] to operate
- It is affected by the complexity 
- Different [[Logic gates]] have various affects on propagation delay
- most simple ones have a delay of t+1 (AND, OR, NOT)
- But some gates are made up of smaller gates:

> [!Example] Prop delay of XOR gate
> ![[propdelayXOR.png|350]]
> - The XOR gate is 4 NAND gates
> - But 2 NANDs run **simultaneously**
> - So the **total propagation delay is +3**


> [!Example] Propagation delay of full [[Adder]]
> ![[propdelayfulladder.png|350]]

