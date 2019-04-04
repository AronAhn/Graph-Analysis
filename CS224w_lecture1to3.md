### Lecture 1
- Bipartite graph: A graph whose nodes can be divided into two disjoint sets U and V s.t. every link connects nodes in U to one in V
  - ex) authors to papaers, actors to movies
- Folded networks: Author collaboration networks, movie co-rating networks


### Lecture 2
- Simplest random graph
  - G_{n, p}: Undirected graph on n nodes and each edge(u,v) appears i.i.d. with probability p
  - G_{n, m}: Undirected graph on n nodes and m uniformly at random picked edges
- The property of G_{n, p}
  - The degree distribution of G_{n, p} follows binomial; P(k) = n-1Ck * p^k * q^(n-1-k)
  - E[C] = k / (n-1)  * 42분
  - Path length: O(log n)
  - CC: C = p = ![](http://latex.codecogs.com/gif.latex?%5Cfrac%20%7B%5Cbar%20k%7D%7Bn%7D)
  - As k, the average degree of the graph, gets larger than 1, *giant conponents* starts to appear
  - Compared to real MSN data with n = 180M
    - [Bad] Degree distribtuion: highly skewed vs bell shape
    - [Good] Avg path: similiar
    - [Bad] Avg CC: MSN han much larger avg CC (.11 vs 8e-08)
    - [Good] Largest comp: It does exist as RG does
    - While G_{n, p} is WRONG, it still turn out to be extremly USEFUL

- Expansion: A measure of robustness
  - def: ![](http://latex.codecogs.com/gif.latex?%5Calpha%20%3D%20%5Cmin_%7BS%5Csubseteqq%20V%7D%5Cfrac%7B%5C%23edges%5C%3Bleaving%5C%3BS%7D%7Bmin%28%7CS%7C%2C%20%7CV%5Csetminus%20S%7C%29%29%7D)
  - To disconnect l nodes, we need to cut >=a*l edges
  - In a graph on n nodes with expansion a for all pairs of nodes *there is a path of length O((logn)/a)*
  - In random graph G_{n, p},
    - For log n > np > c, diam(G) = O(log n / log np)
