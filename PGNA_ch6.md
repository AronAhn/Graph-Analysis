# Chapter 6. Group-Level Analysis

## 6.1. Cohesive subgroups
- Degree centrality looks at the nodes with highest degrees as the most central nodes in the network
- Cohesive subgroups are areas with high density of nodes
- Several techniques have been developed to detect cohesive subgroups within a network such as k-core, cliques, and m-slice

## 6.2. Cliques
- ```nx.find_cliques(g)```

## 6.3. Clustering coefficient
- CC is the fraction of the node's neighbors that are also neighbors with each other
- This metric can be applied either locally or globally
  - Locally, it emphasized the neighborhood of a node
  - Globally, it is the level of clustering in a graph
- ```nx.clustering(g)```

## 6.4. Triadic anaylsis
- A triad is a subgraph with three nodes: a focal(ego), an altar, and a third node
- It is the smallest graph structure that has more than two ndoes
- The four cases of triad are; Complete, open, closed, and unconnected

## 6.5. Structural holes
- A hole in the ego network of a node such that two of its neighbors cannot connect directly

## 6.6. Brokerage
- Brokerage focuses on social relations in network as channels of exchange
- It measures ego's potential to induce and exploit competition between actors in a triad
- Another important concepts that is related to brokerage is *aggregate constraint*
  - The sum of the dyadic constraint on all the ties of a particular node
