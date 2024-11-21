A graph is a mathematical structure for representing relationships. They are used to model many real-world scenarios.

## Mathematical definition
- A graph is an [[tuples#Ordered pair|ordered pair]] $G=(V,E)$ where:
	- $V$ is a set of vertices
	- $E$ is a set of edges $E\subset V\times V$ (see [[Cartesian Product]])
- $E$ is a set of either **ordered** or **unordered** pairs:
	- If **ordered**, graph is a *directed graph*
	- If **unordered**, graph is an *undirected graph*
- Each edge is a pair of **start** and **end** nodes (a.k.a. **source** and **sink**)

## Types of graph
- Labelled graph
	- Nodes, edges can have labels (city names, road names etc.)
- Weighted graph
	- Edges can have a numerical value
- Coloured graph
	- Similar to labelling but typically from a small set (e.g. gender)

## Properties
### Paths
- A **path** is a sequence of edges from one vertex to another
	- The **length** is the number of edges a path contains
- A **cycle** is where a path starts and ends at the same node
- A node is **reachable** from another node if a **path** exists between them
- A path cycle is **simple** if it does not repeat *any* nodes or edges

### Node degrees
- In *undirected* graphs, the **degree** of a node is the number of edges it connects to
- In *directed* graphs, the **outdegree** of is the number of outgoing edges from the given node
- In *directed* graphs, the **indegree** of is the number of incoming edges to the given node

### Adjacency
A graph can be represented as a [[matrix]] $A\in [0,1]^{n\times n}$.
This matrix could look like:

|       | A   | B   | C   |
| ----- | --- | --- | --- |
| **A** | 0   | 1   | 0   |
| **B** | 0   | 0   | 1   |
| **C** | 0   | 0   | 0   |
- In a *directed* graph, a 1 means that the node on the left points to the node at the top. 
	- Here, A->B and B->C.
- In an *undirected* graph, a 1 means there is an edge between the nodes.
	- This matrix could not be an undirected graph as it is **asymmetric**.

If a node A has an edge to node B, A and B are **adjacent**.