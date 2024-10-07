---
tags:
  - 1032-Archi
---
- We can convert between [[bases]] using specific procedures.
### Conversion to [[Bases#Decimal|decimal]]
- Conversion to decimal from other bases involves adding up the numeric values ($2^n$ where n is the position from right to left)
### Decimal to [[Bases#Binary|binary]]
- Decimal to binary has a specific procedure:
	- If the number is even then record 0 else record 1  
	- Divide the number by 2 (discarding the remainder)  
	- Repeat the above steps until the number becomes 0  
	- Read the recorded 0s and 1s in the reverse order
### Binary to [[Bases#Base 8 and 16|hex/octa]]
- Binary to hexadecimal is easy; we split the binary into nibbles (groups of 4) the values of these will be the digits of the hexadecimal.
- We can convert to octal the same way; just group into 3 instead of 4.