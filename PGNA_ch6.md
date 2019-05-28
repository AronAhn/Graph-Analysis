# Chapter 6. Group-Level Analysis

## 6.1. Cohesive subgroups
- Degree centrality looks at the nodes with highest degrees as the most central nodes in the network
- Cohesive subgroups are areas with high density of nodes
- Several techniques have been developed to detect cohesive subgroups within a network such as k-core, cliques, and m-slice

## 6.2. Cliques
- ```nx.find_cliques(G)```

## 6.3. Clustering coefficient
- CC is the fraction of the node's neighbors that are also neighbors with each other
- This metric can be applied either locally or globally
  - Locally, it emphasized the neighborhood of a node
  - Globally, it is the level of clustering in a graph
