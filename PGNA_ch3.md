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

## 3.3. Vertices
  - Deletion of vertex means that removing the vertex and all the edges that contains the vertex
  - For a given vertex x, the number of all adjacent vertices is called "degree" and denoted by d(x)
  - The maximum degree over all vertices is known as the highest degree of G
  - Isolated vetex: A vertex with degree zero
  - Endpoints: Two vertices that are connected by an edge
  - Source/sink vertex: A vertex with in/out-degree zero
  - Cut-vertex: A vertex that if removed, the number of network components increses.
    - Vertex-separator is a collection of vertices that if removed, the graph would be disassembled into small components
  - Labeled vertex: A vertex that is associate with a value that adds further information to the label vertex

## 3.4. Types of Graphs
  - Undirected graph: A graph having edges with no direction
  - Directed graph: A graph having edges with direction
  - Weighted graph: Graphs having weights of real values associated with the edges
  - Planar graph: A graph in a two-dimensional plane with no crossing between ties
    - Ex) The design of electrical circuits, which connect chips, requires that the wires that connect the different components should not cross each other
     <img src ="https://upload.wikimedia.org/wikipedia/commons/thumb/d/dc/Nonplanar_no_subgraph_K_3_3.svg/220px-Nonplanar_no_subgraph_K_3_3.svg.png"> </img>
  - Orthogonal graph: A graph having horizontal and vertical lines
  - Grid-based graph: A graph in which vertices and edges are placed on a two-dimensional grid
  - Simple graph: An directed graph with no loops or multi-edge connectin between any two vertices
  - Regular graph: A graph in which all vertices have the same number of neighbors, which is the degree of each vertex
  - Complete graph: A graph in which any pair of nodes are connected
  - Mixed graph: A graph in which some edges are directed, and others are not
  - Multigraph: A graph which some edges are multiple
  - Half-edge(loose edges) graph: A graph with only one end that is called half-edges or no end (loose edges)
  - Finite and infinite graph: A graph in which V and E are finitite or infinite
  - Connected and disconnected graph: Every pair of distinct vertices in the graph is connected
  - K-vertex/edge-connected graph: If there is no k-1 vertices/edges disconnecting the graph
  	<img src ="https://gateoverflow.in/?qa=blob&qa_blobid=12366043276973393181"> </img>
  - Strongly connected graph: A graph which contains a directed path from u to v and v to u for every pair of vertices u and v
  - Weekly connected graph: Connected graph without direction

## 3.5. Graph Traversals
- Techniques on network analysis require the implementation of one of the traversal algorithms that were designed to either 
  - find the shortest paths between points 
  - to walk across the graph 

### Depth-First Traversal(DFS)
- DFS is a uniformed search technique that systematically traverses nodes until it finds its goal
- The edges that lead to newly discovered nodes are maintained as *discovery edges*
- The edges that are used for back tracking are maintained as *back edges*
- Those two types of edges along with visited nodes establish what is called the *spanning tree*

### Breadth-First Traversal(BFS)
- BFS traverses the network by finding th shortest path from a single-source vertex to every other vertex in the same network segment
- Following page is helpful to understand the concepts of DFS and BFS
  - https://gmlwjd9405.github.io/2018/08/14/algorithm-dfs.html
  - https://gmlwjd9405.github.io/2018/08/15/algorithm-bfs.html

### Dijkstra's Algorithm
- This algorithm finds the shortest path from a givne node to every other node in th same network by considering the length of edges
