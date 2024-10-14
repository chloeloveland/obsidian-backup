- Propagation delay is a the time taken for a [[logical circuit]] to operate
- It is affected by the complexity 
- Different [[logic gates]] have various affects on propagation delay
- most simple ones have a delay of t+1 (AND, OR, NOT)
- But some gates are made up of smaller gates:

> [!Example] Prop delay of XOR gate
> ![[propdelayXOR.png|350]]
> - The XOR gate is 4 NAND gates
> - But 2 NANDs run **simultaneously**
> - So the **total propagation delay is +3**


> [!Example] Propagation delay of full adder
> ![[Pasted image 20241014154510.png|350]]
> - at AB, t+0
> - at P, t+3
> - 
