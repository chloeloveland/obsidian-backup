---
tags:
  - 1034-Programming
---
There are several ways of representing a [[Graph]] in code.

## Adjacency Matrix
- A graph can be represented using a 2d array which stores an [[Graph#Adjacency|adjacency matrix]]
- This is sometimes used in low-level languages
- For *some algorithms* (such as path length) this is <mark class="hltr-green">very fast</mark>
- However its <mark class="hltr-red">memory requirement grows quadratic to graph size</mark> 
	- not practical for large graphs

> [!info] 
> In python, arrays do not have built in support. We can instead use **lists** and treat them like arrays.

## Adjacency lists
- Can also be represented by mapping each source node to sink node
	- Using a [[Dictionary]]
- Avoids iteration through [[Graph#Mathematical definition|V]]

## Mapping from sources to dictionaries of sinks 
- Similarly to [[Graphs in code#Adjacency lists|adjacency lists]], we can instead map a dictionary where each sink is itself a dictionary.
- This means edges can store [[Graph#Types of graph|attributes]] such as **labels** or **weights**.

## Using a graph class
- The [[#Mapping from sources to dictionaries of sinks|previous implementation]] works very well to capture the structure of graphs
- However it becomes confusing for complex graphs with lots of [[Graph#Properties|properties]]
- So we should encapsulate this complexity in a class
	- There are many existing python libraries that do this, including:
		- pygraphviz ([doc](https://pygraphviz.github.io/documentation/stable/index.html))
		- networkx ([doc](https://networkx.org/documentation/stable/reference/introduction.html))
- The best way to do it