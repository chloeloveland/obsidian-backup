---
tags:
  - 1032-Archi
---
- Parity bit is a form of [[error detection]]
- It is an additional bit added to the back (left) of a binary value
- Parity bit -> 0|0000000

### Even parity
- Total number of ones should be **even**
- So if number of ones is **3**, parity is 1
- if number of ones is **2**, parity is 0
- EXAMPLE: 0100101 -> 10100101

### Odd parity
- Total number of ones should be **odd**

Usually even parity is used.

### Error correction using parity
![[Pasted image 20241021095604.png|left|350]]

![[Pasted image 20241021100455.png|left|350]]

### Logical implementation
- Parity can be implemented as a [[logical circuit]]

> [!Diagram] Parity circuit - 3 bit
> ![[Pasted image 20241021100639.png|350]]

> [!Diagram] Parity circuit - 4 bit
> ![[Pasted image 20241021100740.png|350]]

