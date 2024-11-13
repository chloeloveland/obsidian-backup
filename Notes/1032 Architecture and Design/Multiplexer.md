---
tags:
  - 1032-Archi
---
- A multiplexer is a [[Logical circuit]] which takes a number of inputs and forwards a selected input to the output line based on the combination of inputs.
- is also known as a **data selector**, or **mux** in shorthand
- The circuit which performs the inverse function is the [[Demultiplexer]].
- It operates by using a control signal which selects which output line receives the data.
	- If we have 4 data channels, we need 2 selector lines (00,01,10,11) :)

>[!Example] A 4 to 1 multiplexer
>![[multiplexer4-1.jpg|450]]

>[!tip] Application
>- A multiplexer is often used to create the **majority** function.
>- This is used after data transmission for [[error detection]].
>- It is also often used to have multiple data streams over a single line:
>![[Telephony_multiplexer_system.gif]] ^ef4llu


