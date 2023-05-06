# Agglomerative Hierarchical Clustering (Bottom Up)
Agglomerative hierarchical clustering is a clustering algorithm that works by iteratively merging smaller clusters into larger ones. The algorithm starts by treating
each data point as a separate cluster, and then repeatedly merges the two closest clusters together until all data points are in a single cluster.

The merging process in agglomerative hierarchical clustering can be visualized as a dendrogram, which is a tree-like diagram that shows the hierarchical relationships 
between clusters. The dendrogram starts at the bottom with each individual data point as a separate cluster, and then branches upwards as clusters are merged together. 
The height of each branch on the dendrogram represents the distance between the clusters being merged, with shorter branches indicating closer similarity.

**Agglomerative hierarchical clustering can be done in two ways:**

**Single Linkage:** In single linkage, the distance between two clusters is defined as the distance between the two closest data points in the two clusters.

**Complete Linkage:** In complete linkage, the distance between two clusters is defined as the distance between the two farthest data points in the two clusters.

Once the distance between clusters is defined, the algorithm selects the two closest clusters and merges them into a single larger cluster. This process is repeated
until all data points belong to the same cluster.

One of the advantages of agglomerative hierarchical clustering is that it can produce a hierarchy of clusters, which can be useful for understanding the relationships 
between different clusters at different levels of granularity. 
![16-Hierarchical-Clustering-Dendrogram](https://user-images.githubusercontent.com/128781536/236629241-8b9f0b18-94b5-4d42-9643-f479e8f00692.png)

## 4 step algorithim for Hierrarchical Agglomerative clustering

1) Initially each data point forms a cluster.
2) Compute the distance matrix between the clusters.
3) Repeat
- Merge the two closest clusters
- Update the distance matrix
4) Until only a single cluster remains.

Different definitions of the distance leads to different algorithms.


Step 1: Assign each data point to its own cluster
|   1   |   2   |   3   |   4   |   5   |   6   |
--------------------------------------------------
|   A   |   B   |   C   |   D   |   E   |   F   |

Step 2: Compute the pairwise distances between clusters using a distance metric, such as Euclidean distance

|       |   A   |   B   |   C   |   D   |   E   |   F   |
-----------------------------------------------------------
|   A   |   -   | 3.16 | 5.00 | 4.12 | 5.39 | 7.07 |
|   B   |   -   |   -   | 4.24 | 3.16 | 4.69 | 6.32 |
|   C   |   -   |   -   |   -   | 2.24 | 2.24 | 4.47 |
|   D   |   -   |   -   |   -   |   -   | 3.16 | 4.24 |
|   E   |   -   |   -   |   -   |   -   |   -   | 2.24 |
|   F   |   -   |   -   |   -   |   -   |   -   |   -   |

Step 3: Merge the two closest clusters into a larger cluster, based on the pairwise distances computed in Step 2. The algorithm repeats this step until all data points belong to the same cluster.

Here's an example of how the algorithm merges the clusters:

|   1   |   2   |   3   |   4   |   5   |   6   |
--------------------------------------------------
|   A   |   B   |   C   |   D   |   E   |   F   |

Step 1: Merge clusters C and E, since they are the closest together with a distance of 2.24


| 1 | 2 | 3 | 4 | 5 |
| A | B | C,E | D | F |

Step 2: Merge clusters D and F, since they are the closest together with a distance of 4.24
| 1 | 2 | 3 | 4 |
| A | B | C,E | D,F |



Step 3: Merge clusters B and D/F, since they are the closest together with a distance of 4.24
| 1 | 2 | 3 |
| A | B,D,F | C,E |



Step 4: Merge clusters A and B/D/F, since they are the closest together with a distance of 3.16
| 1 | 2 |
| A,B,D,F | C,E |



At this point, all data points belong to the same cluster. The dend
