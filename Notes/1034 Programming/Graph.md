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

## Properties of graphs
- A **path** is a sequence of edges from one vertex to another
	- The **length** is the number of edges a path contains
- A **cycle** is where a path starts and ends at the same node
- A node is **reachable** from another node if a **path** exists between them
- A path cycle is **simple** if it does not repeat *any* nodes or edges

### Node degrees
- In *undirected* graphs, the **degree** of a node is the number of edges it connects to
- In *directed* graphs, the **outdegree** of is the number of outgoing edges
- In *directed* graphs, the **indegree** of is the number of incoming edges