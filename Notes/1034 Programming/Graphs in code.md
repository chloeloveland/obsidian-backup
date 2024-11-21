---
tags:
  - 1034-Programming
---
There are several ways of representing a [[graph]] in code.

## Adjacency Matrix
- A graph can be represented using a 2d array which stores an [[Graph#Adjacency|adjacency matrix]]
- This is sometimes used in low-level languages
- For *some algorithms* (such as path length) this is <mark class="hltr-green">very fast</mark>
- However its <mark class="hltr-red">memory requirement grows quadratic to graph size</mark> 
	- not practical for large graphs

> [!info] 
> In python, arrays do not have built in support. We can instead use **lists** and treat them like arrays.

### Implementation

```
# vertices:
V = ["A", "B", "C", "D", "E", "F"]
# adjacency matrix:
E = [[0,   1,   0,   0,   0,   0], # "A"
     [0,   0,   1,   0,   0,   0], # "B"
     [0,   0,   0,   0,   1,   0], # "C"
     [0,   1,   0,   0,   0,   0], # "D"
     [0,   0,   0,   1,   0,   1], # "E"
     [0,   0,   0,   0,   0,   0]] # "F"

def out_edges(V, E, i):
    for j in range(len((V)):
        if E[i][j]:
            yield i, j
```

## Adjacency lists
- Can also be represented by mapping each source node to sink node
	- Using a [[dictionary]]
- Avoids iteration through [[Graph#Mathematical definition|V]]

### Implementation
```
# graph
G = {"A": ["B"],
     "B": ["C"],
     "C": ["E"],
     "D": ["B"],
     "E": ["D", "F"],
     "F": []}

def out_edges(G, source):
    for sink in G[source]:
        yield (souce, sink)

def out_degree(G, source):
    return len(G[source])
```

## Mapping from sources to dictionaries of sinks 
- Similarly to [[Graphs in code#Adjacency lists|adjacency lists]], we can instead map a dictionary where each sink is itself a dictionary.
- This means edges can store [[Graph#Types of graph|attributes]] such as **labels** or **weights**.

### Implementation
```
G = {"A": {"B": "edge A->B"},
     "B": {"C": "edge B->C"},
     "C": {"E": "edge C->E"},
     "D": {"B": "edge D->B"},
     "E": {"D": "edge E->D", "F": "edge E->F"},
     "F": {}}

def out_edges(G, source):
    for sink in G[source]:
        yield (source, sink)
```


## Using a graph class
- The [[#Mapping from sources to dictionaries of sinks|previous implementation]] works very well to capture the structure of graphs
- However it becomes confusing for complex graphs with lots of [[Graph#Properties|properties]]
- So we should encapsulate this complexity in a class
	- There are many existing python libraries that do this, including:
		- pygraphviz
		- networkx