---
tags:
  - 1031-Fundamental
---
## Basic set expression
- The simplest form of expressing a set is writing down all its components
- If a set has a pattern and is very long or infinite, we can express it with an ellipsis instead 

## Set Comprehension

- for large sets we may use set comprehension:
- e.g {x I x∈{1, ..., 100}, x<10 and x is odd}
- this is defining a set using another set
- so the result is a set which contains the odd numbers 1-10
- the format for this notation is as seen:
- so the result set is 42 , 22 = 16, 4

## Recursion

- Defining a set via recursion involves 2 (3) steps
    1. base case
    2. recursive case - define how new values are generated from the base case
    3. (nothing else in set) - this is usually left implied

> [!Example]
>  Here is a recursive definition for the set N of natural numbers:
>  1. Know that 0 ∈ **N**
> 2. If we already know x ∈ $\mathbb{N}$ then we know (x+1) ∈ $\mathbb{N}$.
> 3. Nothing else is in set $\mathbb{N}$
