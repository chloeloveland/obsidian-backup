- Hamming code is an error-correcting code.
- It works by encoding four bits of data into seven bits (at the smallest size) by adding three [[Parity bit|parity bits]].

## Usage
![[Pasted image 20241021100455.png|left|350]]
- The data bits are the intersecting parts.
- The check bits are the bits exclusive to one set.
- Since it is using [[Parity bit#Even parity|even parity]], the total number of ones in each given set should be even.
- Since this is not true (A and C have odd numbers), we know the data bit at $A\cap C$ is an error.

## Limitations
![[Pasted image 20241021095604.png|left|350]]

As long as only one of seven bits have an error, this can be corrected using the code.
