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

Agglomerative hierarchical clustering **tends to fall in overfitting** if the clustering model is too complex and the algorithm is not properly regularized. This can happen if the number of clusters is too high or if the algorithm is allowed to keep splitting clusters until each point becomes its own cluster. In such cases, the algorithm may memorize the training data and produce clusters that do not generalize well to new data.
