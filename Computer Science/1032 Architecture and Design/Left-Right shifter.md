---
tags:
  - 1032-Archi
---
- Left and right shifting are operations that can be performed on [[Bases#Binary|binary]] numbers
- A left shift multiplies the value by 2, and right shift divides by 2
- A shifter is a [[logical circuit]] which performs these operations

> [!diagram] A shifter circuit
> ![[shifter unit.png|475]]

- The control bit **C** tells the circuit if it is right or left shifting
- if it is 0, the output is shifted to the left
- if it is 1, the output is shifted to the right