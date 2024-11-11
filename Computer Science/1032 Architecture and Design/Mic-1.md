Mic-1 is a simple example processor architecture.

## Data path
The data path of the mic-1 contains 32-bit registers, buses, an ALU and a shifter.

> [!Diagram] Mic-1 Diagram
> ![[th-3208711058.jpg]]

### Buses
There are 2 main buses of 32 lines (or 32 bits) each:
- B bus: connected to the output of the registers and to the input of the ALU.
- C bus: connected to the output of the shifter and to the input of the registers.

### Registers
Registers are selected by 2 control lines: one to enable the B bus and the other to enable the C bus. The B bus can be enabled by just one register at a time.  

The MBR register is a read only register, and it contains 2 control lines. Since it is an 8-bit register, its output is connected to the least significant 8 bits of the B bus. It can be set to provide its output in 2 ways:


