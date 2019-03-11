# Sampling from Large Graphs
- 10.1145/1150402.1150479
- https://scinapse.io/papers/2146008005

## Abstract
  - Given a huge real graph, how can we derive a representative sample?
  - Questions
    - Which sampling method to use
    - How small can the sample size be
    - How to scale up the measurements of the sample(e.g. ,the diameter) to get estimates for the large graph
  - Conclusions
    - Sampling strategies based on *edge selection do not perform well*
    - Simple uniform *random node selection performs surprisingly well*
    - Best performing methods are the ones based on *random-walks* and *Forest Fire*
## Introduction
  - How do we measure the goodness of a sampling method?
    - Scale-down goal: Sample graph S have similar properties as compared to the original graph G
    - Back-in-time goal: Sample graph S to be similar to what the graph G looked like *back in the time* when it had the size of S
 - We perform systematic evaluation of sampling algorithms
    - non-trivial statistical evaluation methods: The Kolmogorov-Smirnov D-statistic and random walk inspired ieas
  - Best performing sampling methods are the following
    - For the scale-down sampling goal, methods based on *random walks* perform best
    - They are biased towards high degree nodes and give sampled graphs that are connected
    - For the Back-in-time-sampling goal, *Forest Fire* type sampling and sampling based on *PageRank* score of a node perform best

## Proposed method
### Evaluaion techniques
  - Criteria for a static snapshot of a graph
    - S1: In-degree disr: For every degree d, we count the n of nodes with in-degree d
    - S2: Out-degree distr
    - S3: The dist of sized of weakly connected components(WCC)
    - S4: The dist of sized of strongly connected conponents(SCC)
    - S5: Hop-plot: The  of P(h) of reachable pairs of nodes at distance h or less; h is the n of hops
    - S6: Hop-plot on the largest WCC
    - S7: The dist of the first left singular vector of graph adjc matrix
    - S8: The dist of singular values of the graph adjc matrix versus the rank
    - S9: The dist of the clustering coefficient Cd
  - Criteria for temporal graph evolution
    - T1: Densification power law(DPL)
      - n of edges versus the n of nodes over time
      - DPL stats that ![](http://latex.codecogs.com/gif.latex?e%28t%29%20%5Cpropto%20n%28t%29%5Ea)
      - The densification exponent a is a typically greater than 1, implying that the average degree of a node in the graph is increasing over time
    - T2: The effective diameter, which is defined as the minimum number of hops in which 90% of all connected pairs of nodes can reach each other
      - It has been observed that the effective diameter generally shrinks or stabilized as the graph grows with time
    - T3: The normalized size of the largest connected component(CC) over time
    - T4: The largest singular value of graph adjacency matrix over time
    - T5: Average clustering coefficient C over time
  - Statistical test for graph patterns
    - To compare the two graph pattern, we use the *Kolmogorov-Smirnov D-statistic*
    - We simply use it to measure the agreement between the two dist
    - It is defined as ![](http://latex.codecogs.com/gif.latex?D%20%3D%20max_x%5C%7B%7CF%27%28x%29%20-%20F%28x%29%7C%5C%7D), where x is over the range of the r.v,  F and F' are the two ecdf of the data
