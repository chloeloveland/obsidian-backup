## Intro

- A set is a collection of objects
- Can contain infinite elements
- Elements are unordered - more like a bag than a list
- There are no duplicates in a set

## Common Sets

- ℕ is the natural numbers set (1, 2, 3, ...)
- ℤ is the integers set (-1, 0, 1, ...)
- ℚ is the rational numbers (nums that can be expressed as a fraction)
- ℝ is the real numbers (a number on the number line, any 1 dimensional value)

## Set Notation

- Can be notated as {1,2,3,4} or {1,2,...,100}
    - See [[#Set Comprehension]] and [[#Recursion]]
- ∈ denotes membership e.g $2 ∈ ℕ$
    - This means the element 2 is in the set ℕ
- ∉ denotes lack of membership e.g -1 ∉ ℕ
- ⊂ denotes subset e.g ℕ⊂ℤ, {1,2} ⊂ {1,2,3}
    - This means the whole set ℕ is in ℤ
- ⊆ denotes subset or equal (so the sets can actually be identical) whereas ⊂ is a 'proper' subset
- ⊄ means not a (proper) subset
- **P**(A) is a power set. A power set is a set which contains all possible subsets of its defining set.
- AxB denotes the cartesian product of sets A and B
- A line before and after a set - e.g |AxB| - is the cardinality (size) of the set
- $\cup$ denotes union
    - union is the combination of sets; ${A \cup B}$ is all the elements of both A and B
- $\cap$  denotes intersection 
    - intersection returns the elements two sets have in common
- \ denotes difference
    - difference finds the set of elements that are not common
    - ${A\backslash B}$ essentially returns A take away B
    - so if A = {1,2,3} and B= {1,2}, then ${A\backslash B}$ = {3}
    - note that set difference is **non-commutative**
    - So ${A\backslash B \neq B \backslash A}$

## Set Comprehension

- One way to show the members of a set is to list them
- this does not work for large sets
- for this we may use set comprehension:
- e.g {x I x∈{1, ..., 100}, x<10 and x is odd}
- this is defining a set using another set
- so the result is a set which contains the odd numbers 1-10
- the format for this notation is as seen:
- so the result set is 42 , 22 = 16, 4

## Cardinality

- Cardinality is the size of a set
- it ignores duplicates (because they do not exist in sets)
- so the set {1,2,3,4,4} has a size of 4
- the cardinality of ℕ is infinite

## Tuples

- A tuple is a pair of values, where each is from its own set
- if set A = {tea, coffee} and set B = ℝ, then a tuple from these sets could be (tea, 1.2) or (coffee, 2) etc.
- **in a tuple order is considered, unlike a set**

> [!Why is this useful?]
> - Sets and tuples can be used to abstractly model systems
> - Tuples for objects and sets for collections of objects
> - So we could have tuples which represent drinks and their prices
> - and a set which contains all of these different drinks options

## Cartesian Product

- Notation is AxB where A and B are sets
- This product is a set which contains all possible tuples of (element from A, element from B)

> [!Example]
> - Let $A = {1, 2, 3}$ and $B = {a, b}$.
> - $A\times B = {(1, a), (1, b), (2, a), (2, b), (3, a), (3, b)}$**
- Since order is considered in Tuples, AxB is **not** the same as BxA.
- To find the cardinality of the product of two sets, we just multiply the cardinalities of the individual sets together. e.g $|A| = 2$ and $|B| = 3$, then $|A\times B| = 6$> 
- To find the cardinality of the power set, we do 2^(cardinality of set). For example, $|A| = 10$, then $|P(A)| = 2^{10}$. 

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

