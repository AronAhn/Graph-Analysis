# Chapter 2. Network Basics

## 2.1. What is a Network?
- A network can be a specialized type of mathematical graph or interconnected systems
- Network nodes may represent web pages, people, organizations, ...
properties which are more relevant 
## 2.2 Types of Networks
- Information networks: Man-made networks in which data items are linked together in some way.
  - World Wide Web(WWW), Facebook, Twitter, ...
- Technological networks: Man-made networks that are designed to distribute commodity or resources
  - Internet, transportation networks, telephone networks, ...
- Biological networks: Networks that represents patterns of interaction between biological elements
- Social networks: Network in which vertices represent people and edges represent some form of social interaction between vertices including friendship, kinship, ...
- Complex networks: Wikipedia defines complex networks as networks with non-trivial topological features
  - These features do not occur in simple networks such as lattices or random graphs but often happen in real graphs
  - Biological networks, brain networks, social networks, ...
  
## 2.3. Properties of Networks
- Network static properties are fixed: They are the properties of nodes and edges and do not change over time once the network is established
- Network dynamic properties are not fixed: They can be processes running on the underlying network substrate
- All types of networks share the folloing common characteristics:
  - Transitivity(clustering): If node A is connected to node B and node B is connected to node C, then there is a high probability that node A is also connected to node C
  - Network robustness and vulnerability: Networks are susceptible to dynamic topological changes caused by external forces such as node removal
    - Node removal can be the result of the followings:
      - Error: A random removal of nodes
      - Attack: A selective removal of most connected nodes 
  - Mixing patterns: The tendency of vertices to be connected to other vertices that are like (or unlike) them in some way
  - Community structure: Networks may have high edge density between nodes of the same group while having low dege density between nodes from different groups
  - Additional properties which are more relevant to large networks
  - The tendency to establish groups of acquaintances and friends to from cliques where everyon knows everyone else
  - Node degree tends to show a power law distribution, which is the prob that a random node has a certain number of edges
  
## 2.4. Network measures
- Aggregate constraint: The sum of the dyadic constraint on all the ties of a paiticular vertex
- Average degree: A measure of the structural cohesion of a network
- Degree distribution: Frequency of the degrees of nodes
  - Graphs with power law degree dist are called scale-free
- Average shortest path: Average shortest path length over all pairs of nodes characterized how large the world represented by the network
- Eccentricity: Max shortest path length from each node
- Diameter: The longest shortest-path distance over all pairs of nodes in the network, or max eccentricity in the network
  - Radius is the min eccentricity in the network
- Dyad: A pair of nodes connected via one or more ties
- Dyadic constraint: The dyadic constraint on vertex u projected by the tie between vertex u and vertex v is the extent to which u has more and stronger ties with neighbors that are strongly connected with vertex v  
- Geodesic: A geodesic is the shortest path between two vertices
- Average geodesic distance: The mean of the shortest path lengths among all connected pairs in the ego network
  - Ego network: e networks consisting of a single actor(ego) together with the actors they are connected to (alters) and all the links among those alters
  *Everett, M.G., & Borgatti, S.P. (2005). Ego network betweenness. Social Networks, 27, 31-38.*
- Multiplicity: The number of times a particular line occurs in a network
- Popularity: The popularity of a vertex in a directed network is the number of arcs that it receives
- Triad: A subnetwork consisting of three nodes

## 2.5. NetworkX
- NetworkX is the Python-based graph toolkit and is a type of memory graph databases
- Graph types available from NetworkX packages
```
import networkx as nx
print([s for s in dir(nx) if s.endswith('graph')])
```

## 2.6. Matrices
- A matrix is an alternative way to represent and summarize network data
- It is an array of elements that contains the same information as a graph
- Types of matrices in social networks
  - Adjency matrix: A matrix with rows and columns at plot by nodes, where elements ![](http://latex.codecogs.com/gif.latex?A_%7Bij%7D) shows the number of links going from node i to node j
    - It is not a good choice for large graph since because of the sparseness
  - Edge list matrix: The list of edges represented as a tuple consisting of starting point, destination and attribute(optional)
  - Adjacency list: A list of links whose element "i->j" show a link going from node i to node j
  <img src ="https://pythonandr.files.wordpress.com/2016/07/adjacencylist.png"> </img>
  - Numpy matrix, Sparse matrix

## 2.7. Basic Matrix Operations
- Matrix permutation: The rearrangement of rows and columns in a matrix.
  - This is done at times when network tie patterns are not clear until we permute both the rows and the columns of the matrix
- Matrix transpose, addition, subtraction, multiplication

## 2.8. Data Visualization
- Trees, undirected graphs in which every two vertices are connected by one simple path, are used at some times for data visualization and particularly when the dataset is small
  - Trees can be polytree, rooted, labeled, recursive, directed, free, binary, or ternary
- Other visualization tools include maps and hybrid approaches, multidimensional visualization techniques that used in both graphs and maps
