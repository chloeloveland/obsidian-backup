There are several ways of representing a [[graph]] in code.
## Matrix
- A graph can be represented using a 2d array which stores an [[Graph#Adjacency|adjacency matrix]]
- This is sometimes used in low-level languages
- For some algorithms (such as path length) this is very fast
- However its memory requirement grows quadratic to graph size 
	- not practical for large graphs

> [!info] 
> In python, arrays do not have built in support. We can instead use lists and treat them like arrays.
