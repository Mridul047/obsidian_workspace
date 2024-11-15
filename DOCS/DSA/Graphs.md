## Definition: 
* Graphs are basically collection of nodes connected via edges.
* Graphs can be an open structure like Binary Tree.
* Graphs can have 1 or multiple cycles.

## Types Of Graphs:
* Directed Graph
	* Directed Acyclic Graph
* Undirected Graph
	* Undirected Cyclic Graph

## Degree Of Undirected Graph:
* Number of edges attached to a given node.
* Total Degree of Graph = 2 x E

## Degree Of Directed Graph:
* Indegree : Number of inward edges of a given node.
* Outdegree: Number of outward edges of a give node.

## Weighted Edges:
* Weights are numbers assigned to edges in a graph.
* If no weight is specified then the default weight is considered as 1.

## Connected Components in Graphs:
* A graph can be broken down into multiple graphs which may not be connected.
* To traverse such components we can use Visited-Array.
* Visited-Array should be initialized with 0 value & size  = Nodes + 1.
* Index of this array signifies the Node in connected components.
* For every index in Visited-Array we will change value to 1 if the component as been traversed. 