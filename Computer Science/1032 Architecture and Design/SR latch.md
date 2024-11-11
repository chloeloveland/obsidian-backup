---
tags:
  - 1032-Archi
---
- SR latch is a form of simple [[memory]]
- The SR latch is an example of a [[Sequential Circuit]]; it includes *feedback* and *clocks*
> [!Diagram] An SR latch
> ![[SRlatch.png]]
> - S stands for SET
> - R stands for RESET
> - Q will remain at the same state until either SET or RESET is true
> - SET makes the value 1 and RESET 0


> [!danger] 
> S and R should **never** be true at the same time! 
> This produces an invalid output


> [!Diagram] A clocked SR latch
> ![[clockedSRlatch.png|450]]
> - this latch includes a clock which means it can hold a bit in memory until the next clock cycle

