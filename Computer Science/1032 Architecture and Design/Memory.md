- In computing, memory is any way of storing binary data
- The simplest example of this is the [[SR latch]]
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
> ![[Pasted image 20241014163056.png|450]]
> - this latch includes a clock which means it can hold a bit in memory until the next clock cycle

