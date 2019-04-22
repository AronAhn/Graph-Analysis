# Chapter 1. Theoretical Concepts of Network Analysis

## 1.1 Sociological Meaning of Network Relations
- A *network* is a set of relations between actors.
- *Actors* can mean individuals, groups, organizations, states, etc.
- Relations between nodes in a network are called *ties*.
  * Ties can mean kinship with people, affection, enmity, ...
  * Ties can have *directions*.
  * Relations between individuals may vary in *intensity*.
  * It is also possible to have more than one *kind* of relation.

## 1.2. Network Measurements
  - Network connections: transitivity, multiplexity, homophily, dyads, mutuality, balance, triads, reciprocity
  - Network distribution: the dist between nodes, degree cntly, close cntly, between cntly, eigen cntly, PageRank, gedesic dist, shortest path, eccentricity, density
  - Network segmentation: cohesive subgroups, cliques, clustering coefficient, k-cores, core/periphery, blockmodel, hierarchical clustering

### 1.2.1. Network Connections
  - Transitivity: (3 x n of triangles) / (n of connected triples)
    - A value of 1 means that the network contains all possible edges
  - Multiplexity: Ties with more than one dimension are multiplex <-> uniplex
  - Homophily: The tendency of individuals to connect with others who share the same attitudes and beliefs
  - Dyad: A pair of actors in a network potentially connected by a social relation
  - Triad: A network structure consisting of three actors and three dyads
    - odd/even number of +/- edges are balanced/unbalanced
  - Reciprocity: A measure of the tendency towards building mutually directed connections between two actors
    - For a given node v, reciprocity is the ratio between the n of nodes which have both incoming and outgoing connections from/to v, to the n of nodes which only have incoming connection from v
    - For a entire network, reciprocity is calculated as the fraction of edges that are reciprocated

### 1.2.2. Network Distribution
  - Distance between two nodes
    - Geodesic distance: Number of links in the shortest path from node i to node j
    - Eccentricity: The maximum distances from a given node to all other nodes in a network
    - Network diameter: the highest eccentricity of its nodes, which represents the maximum distance between nodes
  - Degree centrality: The importance of a node is determined by how many nodes it is connected to
    - ![](http://latex.codecogs.com/gif.latex?d%28i%29%20%3D%20%5Csum_i%20m_%7Bij%7D)
    - In social networks, node degree distribution follows a power law distribution
    - For directed networks, in-degree is often used as a proxy for popularity
  - Closeness centrality: To a particular actor, how close other actors are
    - ![](http://latex.codecogs.com/gif.latex?C%28i%29%20%3D%20%5Csum_j%20d_%7Bij%7D%20%5Cpropto%20%5Cfrac%7B1%7D%7Bcentralirity%7D)
    - High-scoring nodes usually have shorter paths to the rest of nodes in the network
  - Betweenness centrality: How important an actor is, as a link between different networks
    - Calculation example: https://youtu.be/0CCrq62TF7U?t=482
    - It shows which nodes are likely pathways of information
    - Also, it can be used to determine how a graph will break apart of nodes are removed.
    - Similarly it is a way to identify those who act as *bridges*(boundary spanners)
  - Eigenvector centrality: The centrality of a person with regard to the global structure of the network
  - PageRank: The importance of a web page by considering the probability that a user visits this page based on the hyplink
    - A variant of the eigenvector centrality
    - ![](http://latex.codecogs.com/gif.latex?PR%28u%29%20%3D%20%5Cfrac%7B1-%5Calpha%20%7D%7BN%7D%20&plus;%20%5Calpha%5Csum_v%20A_%7Bvu%7DPR%28v%29/d_%7Bout%7D%28v%29)
      - where a is a damping factor(0<=a<=1), N is the total n of nodes, and d is the degree of outgoing links of v
  - Density: The degree to which network nodes are connected one to another
    - It can be used as a measure of how close a network is to complete
    - ![](http://latex.codecogs.com/gif.latex?D%28G%29%20%3D%20%5Cfrac%7B2m%7D%7Bn%28n-1%29%7D)
      - where m is the n of edges in G

### 1.2.3.  Network Segmentation
  - Cohesive subgroups: Communities in which the nodes are connected to others in the same group more frequent than they are to those who are outside of the group
  - Clique: A maximal complete subgraph(every node is connected)
    - Maximal clique: A clique with size greater than or equal to that of every other clique in the graph
  - K-cores: A connected maximal induced subgraphs having a minimum value greater than or equal to k
    - This means that each node has ties to at least k other nodes
    - K-core can be used by researchers as a sampling technique
  - Clustering coefficient: How much nodes tend to form dense subgraphs
    - For social networks, it can be interpreted as the prob that two friends of a single person are also themselves friends
    - The clustering coefficient C of a node i shows how its neighbors are connected with each other
    - ![](http://latex.codecogs.com/gif.latex?C_i%20%3D%20%5Cbinom%7Bk_i%7D%7B2%7D%5E%7B-1%7DT%28i%29%20%3D%20%5Cfrac%7B2T%28i%29%7D%7BK_i%28k_i-1%29%7D)
      - where T(i) is the n of dist triangles with node i and Ki(ki-1) is the maximum number of possible connections in neighbors of i
    - Network average clustering is defined as ![](http://latex.codecogs.com/gif.latex?C_i%20%3D%20%5Cbinom%7Bk_i%7D%7B2%7D%5E%7B-1%7DT%28i%29%20%3D%20%5Cfrac%7B2T%28i%29%7D%7BK_i%28k_i-1%29%7D)
    - The computation of Ci can be done in time ![](http://latex.codecogs.com/gif.latex?O%28n%5E2%29) in the worst case via counting all edges connected directly to node i
    - The time complexity of a brute-force approach equals ![](http://latex.codecogs.com/gif.latex?O%28n%5E3%29)
    - Another approach using fast matrix multiplication on the adjacency matrix repr in ![](http://latex.codecogs.com/gif.latex?O%28n%5E2.376%29) and ![](http://latex.codecogs.com/gif.latex?O%28n%5E2%29) space
  - Core/Periphery: In any directed, nodes should belong to one of two classes
    - Core: Nodes embedded in a coherent subgraph, or a part of the k-core structure
    - Periphery(light node): Nodes loosely conneted, or which stay outside k-core structure
    - Dynamic network analysis(DNA): The study of nynamic behavior of networks that evolve over time <-> SNA
  - Blockmodeling: An analytic method that uses data partitioning in a social network to classify actor based on their patterns of ties to others
  - Hierarchical clustering: On social networks, hierarchical clustering means that network nodes are partitioned into groups of similar nodes using some distance measure
    - Agglomerative: Cluster all data items into clusters based on a distance metric
    - Divisive: It does the reverse and less commonly used
    - The choice of the n of clusters can be made in different ways such as by calculating the classification error
    - Single-linkage clustering method suffers from *chain effect* and is less suited to detect spherical clusters, it is still more commonly used since it has the ability to detect elongated and irregular cluster
    - Complete-linkage clustering method is not used in general because it is highly sensitive to outliers

## 1.3. Recent Developments in Network Analysis
### 1.3.1. Community detection
  - The task of community detection(or group clustering) is to discover subsets of nodes (clusters) of connected communities
  - Identifying comm is feasible only if the graph is sparse: n of links ~ n of nodes
  - Community: Given graph G=(V;E), a community C can be  defined as a subgraph of G comprising a set ![](http://latex.codecogs.com/gif.latex?V_c%20%5Cin%20V) of objects that share some similarity
  - Algorithms proposed for this purpose can be divided into three categories: divisive, agglomerative, optimization algorithms 
  - Overlapping communities: Communities are expected to allow the sharing of members
  - Girvan and Newman proposed the most popular algorithm
    - There is no need to define the *n of groups* in advance or put *restrictions on their size*
    - They applied a divisive approach
    - Edges are progressiviely removed from the network followed by removing links that lie between communities since they are considered *bottleneck*
  - In computer science, this problem is tackled by decomposing a network into a *predefined n of groups* of nodes
    - These groups almost have the same size, and the n of edges between two groups is minimized
    - First, the network is divided into two gruops.
    - A n of subsequent divisions are conducted next until the required n of group is reached
### 1.3.2. Link Prediction
  - Inferring the links between nodes based on their attributes and the global patterns of links in the social network
  - It can be formally given as follows:
    - Given a network graph G=(V,E), the task here is to predict whether there will be a link between two nodes u and v, where both ![](http://latex.codecogs.com/gif.latex?u%2C%20v%20%5Cin%20V) and ![](http://latex.codecogs.com/gif.latex?e%28u%2C%20v%29%20%5Cnotin%20E)
  - Finding node similarities can be done using measures such as
    - degree distribution, common neighbors, preferential attachment, Jaccard coefficient, Leicht-Holme-Newman Index, and Kart Index
  - Likelihood-based methods make an assumption about the network organization and structure and use that assumption to predict missing links
  - The task of link prediction can be classified into three categories
    - Predict *missing or unobserved* links in a network
    - Predict the links that are likely to be *formed in the near future*
    - Predict whether there will be an *interaction between a pair of nodes* with a previously observed association

### 1.3.3. Spatial Networks
  - A graph in which nodes are embedded in a metric space, which means that the nodes are located in a space equipped with a particular metric

### 1.3.4. Protein-Protein Interaction Networks
  - PPI networks are a type of biological networks

### 1.3.5. Recommendation Systems
  - Recommendation systems are software tools that give suggestions for items that are very likely to be of interest to a particular user
  - Providing recommendations to users can be done in two ways
    - Content-based filtering(CBF): The user will be recommended items similar to the ones he/she preferred in the past
    - Collaborative filtering(CF): It considers a user's past behavior and a similar decision made by other users to predict items that the user may have an interest
  - A user-item network can be built according to what every user has bought/liked in the past
    - The relationship between two users becomes stronger if they have more things in common
    - This network is a type of what is called two-mode network since it has two types of nodes: users and items
