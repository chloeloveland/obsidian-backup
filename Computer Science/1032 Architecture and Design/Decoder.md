- A decoder is a [[logic gates|logical circuit]] which performs the opposite job of an [[encoder]]. It is a combinational circuit that converts $n$ lines of input into $2^n$ lines of output. Let’s take an example of 3-to-8 line decoder.

> [!example]
> 
| A   | B   | C   | F7-F0    |
| --- | --- | --- | -------- |
| 0   | 0   | 0   | 10000000 |
| 0   | 0   | 1   | 01000000 |
| 0   | 1   | 0   | 00100000 |
| 0   | 1   | 1   | 00010000 |
| 1   | 0   | 0   | 00001000 |
| 1   | 0   | 1   | 00000100 |
| 1   | 1   | 0   | 00000010 |
| 1   | 1   | 1   | 00000001 |

