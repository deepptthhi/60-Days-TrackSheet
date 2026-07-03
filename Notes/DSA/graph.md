# Graphs

## What is a Graph?

A graph is a **non-linear data structure** made up of **vertices (nodes)** and **edges (connections)**.

Unlike trees, graphs can have cycles and a node can be connected to multiple other nodes.

Example:

```
A ----- B
|       |
|       |
C ----- D
```



## Things to Remember

- Vertices are the nodes.
- Edges connect the nodes.
- Can be directed or undirected.
- Can be weighted or unweighted.
- Used to represent relationships.



## Types of Graphs

- Directed Graph
- Undirected Graph
- Weighted Graph
- Unweighted Graph



## Graph Traversal

### Breadth First Search (BFS)

- Visits nodes level by level.
- Uses a Queue.

### Depth First Search (DFS)

- Explores one path completely before moving to another.
- Uses a Stack or Recursion.



## Time Complexity

| Operation | Time |
|-----------|------|
| BFS | O(V + E) |
| DFS | O(V + E) |

> **V** = Number of Vertices  
> **E** = Number of Edges



## Advantages

- Represents complex relationships easily.
- Very flexible.
- Useful for solving network problems.



## Where are Graphs used?

- Google Maps
- Social media networks
- Computer networks
- Recommendation systems
- Route planning


## Quick Summary

- Made of vertices and edges
- Can have cycles
- Uses BFS and DFS
- Represents relationships between objects