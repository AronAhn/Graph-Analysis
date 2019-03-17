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
    - Everett, M.G., & Borgatti, S.P. (2005). Ego network betweenness. Social Networks, 27, 31-38.
- Multiplicity: The number of times a particular line occurs in a network
- Popularity: The popularity of a vertex in a directed network is the number of arcs that it receives
- Triad: A subnetwork consisting of three nodes

## 2.5. NetworkX
- A Python language software package and an open-source tool for the creation, manipulation, and study of the structure, dynamics, and functions of complex networks
