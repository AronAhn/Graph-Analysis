# Chapter 4. Social Networks

## 4.1. Social Networks
- A social network is a social composition of actors and relationship defined on them
  - Actors can be persons, places, organizations, roles, etc
  - Relationship can be kinship, friendship, knowledge, acquaintance, correspondence, etc
- Every actor in the network can be connected to one or more other actors to from eventually a structure that represents the social tissu for that individual
- Social networks can be grouped into two types:
  - One-mode network: A network that include one type of nodes to represent actors, subgroups, or communities
  - multi-mode network: A network that include more than one type of nodes

## 4.2. Properties of a Social Network

### 4.2.1. Scale-Free Network
- Networks whose degree distribution obeys a power law: ![](http://latex.codecogs.com/gif.latex?P%28k%29%20%5Csim%20K%5E%7B-%5Cgamma%7D)
- Degree distribution is calculated as follows: ![](http://latex.codecogs.com/gif.latex?P_k%20%3D%20%5Cfrac%7B1%7D%7Bn%7D%20%5C%23%20%5C%7B%20i%7Ck_i%20%3D%20k%20%5C%7D)
- Many network ind=cluding citation network, biological network, WWW graph, ... haver right-skewed or power-law degree distribution
- Power-law distribution means that few nodes account for the vast majority of linke, while most nodes have very few links
- In these network, a small number of well-connected nodes, which is called hubs, significantly reduce the diameter of the entire network


### 4.2.2 Small-World Networks
  - In samll-world networks, most nodes are homogenoeous and can be reached by a small number of steps
  - The distance between any two nodes grows proportionally to the logarithm of order of the network
  - Those have many local links and few long-range *shortcuts*
  - High CC, short average path length, over abundance of hub nodes
  - Dense clusters loosely connected by boundary spanners(connectors)
    - They are uniform but decay exponentially
  - Famous graphsin this category is *Watts-Strogats(WS) small-world graph*
    - It has three parameters; n,k, and seed

### 4.2.3 Network Navigation
- Dunbar's number; A cognitiver limit to the number of individuals with whom one can maintain stable social relationships

## 4.3 Data Collections in Social Networks
- Traditional methods to collect social data include
  - Questionnaires, interviews, observation, archival records, ...

## 4.6 Online Social Data Colection
- Beyond the traditional methods of collecting social data, online data can be collected by the following methods
  - APIs, web crawlers, online surveys, edployed applicatoins

## 4.7 Data Sampling
- The three most frequently techniques used here are
  - Node sampling: A limited subset of nodes alongside their links are chosen to be the sampled data
  - Link sampling: A subset of link is selected to represent the sampled data
  - Snowball sampling
    - It starts with a set of sampled nodes alongside their neighbors: the first-order zone of the network
    - The nodes in this zone are sampled, and all their connectiosn are extracted to from the second-order zone
    - This process is done several times and leads eventually have a network of several zones

## 4.8 Social Network Analysis
  - The four distinctive characteristics; systematic relational data, structural intuition, graphical models, and mathematical models
  - The levels of analysis: micro, meso, and macro, in addition to the interactions between them

## 4.9. Social Netwrok Analysis vs Link Analysis
  - Link analysis allows for different types of nodes and edges to coexist on the same network which amy produce invalid results
  - The way that SAN uses to solve the problem of having a network with different types of nodes and edges is by using multimode networks
