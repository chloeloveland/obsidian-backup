There are several ways of representing a [[graph]] in code.

## Using Adjacency Matrix
- A graph can be represented using a 2d array which stores an [[Graph#Adjacency|adjacency matrix]]
- This is sometimes used in low-level languages
- For some algorithms (such as path length) this is very fast
- However its memory requirement grows quadratic to graph size 
	- not practical for large graphs

> [!info] 
> In python, arrays do not have built in support. We can instead use **lists** and treat them like arrays.

### Implementation
> [!Example] Matrix implementation in python
> ```
># vertices:
V = ["A", "B", "C", "D", "E", "F"]
> # adjacency matrix:
> E = [[0,   1,   0,   0,   0,   0], # "A"
>      [0,   0,   1,   0,   0,   0], # "B"
>      [0,   0,   0,   0,   1,   0], # "C"
>      [0,   1,   0,   0,   0,   0], # "D"
>      [0,   0,   0,   1,   0,   1], # "E"
>      [0,   0,   0,   0,   0,   0]] # "F"
> 
> def out_edges(V, E, i):
>     for j in range(len((V)):
>         if E[i][j]:
>             yield i, j

## Adjacency lists
- Can also be represented by mapping each source node to sink node
	- Using [[dictionary]]