# Chapter 3. Graph Theory

## 3.1. Origins of Graph Theory
- A graph is a mathematical object that describes relationships between items
- Graph theory has become useful in the study of social networks for several reasons
  - It provides a *vocabulary* that can be used to label and denote many social structural properties
  - It provides the use of many *mathematical operations* and *ideas* that help quantify and measure many of the social strucctural properties
  - Graph theory gives a way to *prove theorems* of graphs and *representations of social structure*
- Classes of problems related to graph study fall into a few categories
  - Existence: Problms that attempt to determine if a path, a vertex, or a set exists, particularly if there is a constraint
    - What is constraint??
  - Construction: Given a set of paths and vertices, and within given constraint, how to construct a graph?
  - Enumeration: Problems that attempts to determine how many vertices and edges exist, given a set of constraints
  - Optimization: Problems that attempt to find the shortest path between two nodes

## 3.2. Graph Basics
- Trail: A walk that does not go through the same link more than once
- *Path*: A walk that does not go through the same node more than once
- Cycls: A walk that starts and ends at the same node and that does not go through the same node on its way

## 3.3 Vertices
  - Deletion of vertex means that removing the vertex and all the edges that contains the vertex
  - For a given vertex x, the number of all adjacent vertices is called "degree" and denoted by d(x)
  - The maximum degree over all vertices is known as the highest degree of G
  - Isolated vetex: A vertex with degree zero
  - Endpoints: Two vertices that are connected by an edge
  - Source/sink vertex: A vertex with in/out-degree zero
