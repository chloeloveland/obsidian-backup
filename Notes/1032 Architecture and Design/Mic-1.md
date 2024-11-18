---
tags:
  - 1032-Archi
---
Mic-1 is a simple example processor architecture.

## Data path
The data path of the mic-1 contains 32-bit [[Memory|registers]], buses, an [[Arithmetic Logic Unit|ALU]] and a [[Left-Right shifter|shifter]].

> [!Diagram] Mic-1 Diagram
> ![[th-3208711058.jpg]]

### Buses
There are 2 main buses of 32 lines (or 32 bits) each:
- B bus: connected to the output of the registers and to the input of the ALU.
- C bus: connected to the output of the shifter and to the input of the registers.

### Registers
[[Memory|Registers]] are selected by 2 control lines: one to enable the B bus and the other to enable the C bus. The B bus can be enabled by just one register at a time.

The reading and writing operations are carried out in 1 [[Clock]] cycle. (See [[Mic-1#Timing|timing]])

The MBR register is a read only register, and it contains 2 control lines. Since it is an 8-bit register, its output is connected to the least significant 8 bits of the B bus.

### ALU
The [[Arithmetic Logic Unit]] has:
- 2 32-bit input lines: one for the B bus and one for the bus that is connected directly to the H register.
- 1 32-bit output line, which is connected directly to the shifter.
- 6 control lines aimed to select which operation to perform.
- 2 other output lines for the status flags N (negative) and Z (zero).

### Shifter
The [[Left-Right shifter|shifter]] contains a 32-bit input and output. The shifter contains a 32-bit input and output. The output is connected directly to the C bus.

## Timing

> [!Info] Mic-1 Data Path timing
> ![[Pasted image 20241111095154.png]]
> - The control signals are set up (Δw)  
>- The registers are loaded onto the A and B buses (Δx)  
>- The ALU and shifter operate (Δy)  
>- The results go along the C bus back to the registers (Δz)

## Microarchitecture

> [!diagram] Mic-1 Microarchitecture
> ![[th-2944392813.jpg]]

## Microinstruction Format

> [!info]
> ![[Pasted image 20241111100113.png]]
> - B – Selects B bus source; encoded as shown  
> - Mem – Memory functions  
> - C – Selects which registers written from C bus  
> - ALU – ALU and shifter functions  
> - J – Determines how the next microinstruction selected  
> - Addr – Contains address of potential next microinstruction

## Microinstructions notation

> [!Info] Notation
>![[Pasted image 20241118092343.png]]
>ALU operations. Any of the above operations may be extended by adding "<<8" to them to shift result left by 1 byte.

## Mic-2
The mic-2 iteration adds an instruction fetch unit to the data path, and the A, B, and C latches (one for each bus).
![[Pasted image 20241118093954.png|left]]
![[Pasted image 20241118094614.png|left]]
The latch
## Mic-3
The mic-3 iteration introduces pipelining.