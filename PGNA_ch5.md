# Chapter 5. Node-Level Analysis

## 5.1. Ego-Network Analysis
- A network commonly seen from a particular actor at its center
- Ego network analysis involves the examination of the relations that extend from a particular individual outward to their contacts
- Sociocentric analysis studies the characteristics of the entire network
- Ego centric network analysis examines the subnetwork of one particular node

## 5.2. Identifying Influential Individuals in the Network
- Question: Which nodes, among a large number of connected nodes, are more important?
- *Centrality* is a term used to define the importance of a node

### Degree Centrality
- Degree centrality considers the node with the highest degree (largest number of connections) as the most central node in the network
- ```nx.degree_centrality(g)```

### Closeness Centraliy 
- Closeness centrality measure considers the nodes that have the smallest average path length for the nodes that are links to other nodes
- ```nx.closeness_centrality(g)```

### Betweenness Centrality
- Betweenness centrality relies on the idea that a person is more important if he/she is more intermediary in the network
- ```nx.betweenness centrality(g)```

### Eigenvector Centrality
- It is proportional to the sum of centrality scores of the neighborhood
- ```nx.eigenvector_centrality(g)```

### PageRank
- It represents the likelihood that a random user following links will arrive at a particular page
- For example, a PageRank of .75 means that there is 75% chance that a person clicking on a random link will be directed to the document with the .75 PageRank
- ```nx.pagerank(graph)```

## 5.4. Neighbors
- ```G = nx.Graph(); G.neighbors(0)```

## 5.5. Bridges
- The significance of *bridges* is that they reduce the overall distance between nodes in a network which in turn speeds up information spread throughout the network
- Bridges are links that connect two separate groups

## 5.6. Which Centrality Algorithm to Use?
- *Degree* is a measure of popularity. It determines nodes that can quickly spread information to a localized area
- *Betweenness* is based on the idea that a person is more important if he/she is more intermediary in the network
- *Closeness* is a measure of reach; how fast information will spread to all other nodes from a single node?
- *Eigenvector* is a measure of related importance. Who is closest to the most influential people in the graph?
