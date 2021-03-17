# Community Detection in Artificial and Real Network Topologies
<img src="https://user-images.githubusercontent.com/50949470/111464932-1d025380-872a-11eb-8a23-83ef8fd2fb40.PNG" width="800" height="500">

## Description of Real Nerwork Topologies

### American College Football
Network of American football games between Division IA colleges during regular season Fall 2000, as compiled by M. Girvan and M. Newman. 
The nodes have values that indicate to which conferences they belong.

### Les Miserables
Weighted network of coappearances of characters in Victor Hugo's novel "*Les Miserables*". 
Nodes represent characters as indicated by the labels and edges connect any pair of characters that appear in the same chapter of the book. 
The values on the edges are the number of such coappearances.

### Dolphin social network
Undirected social network of frequent associations between 62 dolphins in a community living off Doubtful Sound, New Zealand.

*For more information about the real topologies visit University of Michigan [Network Datasets](http://www-personal.umich.edu/~mejn/netdata/)*

## Community Detection Algorithms

### Newman-Girvan
The Girvan–Newman algorithm is an Hierarchy-Centric method, that detects communities by progressively removing edges from the original network. 
The connected components of the remaining network are the communities.

The algorithm's steps are:
1) The betweenness centrality of all existing edges in the network is calculated first.
2) The edge(s) with the highest betweenness centrality are removed.
3) The betweenness of all edges affected by the removal is recalculated.
4) Steps 2 and 3 are repeated until no edges remain.

### Spectral Clustering
The Spectral Clustering is a Network-Centric method, taking as an argument the desired number of communities *k* and using the eigenvectors of the Laplacian matrix 
together with an algorithm (usually k-Means), places each node in the appropriate community.

### Modularity Maximization
The Clauset-Newman-Moore greedy Modularity Maximization is a Network-Centric method, that indicates communities on a graph G.
Specifically, it begins with each node in its own community and gradually joins the pair of communities that most increases modularity, until no such pair exists. 
In the end, the pair with the highest modularity is selected by the algorithm.

## Modularity
The metric we use to compare the algorithms is modularity. Modularity measures the strength of a community partition by taking into account the degree distribution.
