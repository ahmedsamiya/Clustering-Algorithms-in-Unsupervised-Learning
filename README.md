# Clustering-Algorithms-in-Unsupervised-Learning
This repository demonstrates the implementation and understanding of three popular clustering algorithms used in **Unsupervised Machine Learning**:
K-Means Clustering
- Hierarchical Clustering
- DBSCAN (Density-Based Spatial Clustering of Applications with Noise)

---

# Table of Contents

- Introduction
- K-Means Clustering
- Hierarchical Clustering
- DBSCAN
- Comparison
- Applications
- Conclusion

---

# Introduction

Clustering is an unsupervised learning technique used to group similar data points into clusters without using labeled data. The goal is to maximize the similarity of data points within a cluster while minimizing the similarity between different clusters.

The three most widely used clustering algorithms are:

- K-Means Clustering
- Hierarchical Clustering
- DBSCAN

---

# 1. K-Means Clustering

## What is K-Means?

K-Means is a centroid-based clustering algorithm that partitions the dataset into **K clusters**. Each cluster is represented by its centroid (mean), and every data point is assigned to the nearest centroid.

---

## Algorithm

1. Select the number of clusters (**K**).
2. Randomly initialize **K** centroids.
3. Assign each data point to the nearest centroid.
4. Update each centroid by calculating the mean of its assigned points.
5. Repeat steps 3 and 4 until the centroids no longer change or the maximum number of iterations is reached.

---

## Objective Function

The algorithm minimizes the Within-Cluster Sum of Squares (WCSS):

\[
J=\sum_{i=1}^{K}\sum_{x\in C_i}||x-\mu_i||^2
\]

where:

- \(K\) = Number of clusters
- \(C_i\) = Cluster i
- \(\mu_i\) = Centroid of cluster i
- \(x\) = Data point

---

## Advantages

- Simple and easy to implement
- Fast for large datasets
- Computationally efficient
- Works well when clusters are spherical

---

## Disadvantages

- Number of clusters (K) must be specified
- Sensitive to outliers
- Sensitive to centroid initialization
- Performs poorly on non-spherical clusters

---

## Applications

- Customer Segmentation
- Market Analysis
- Image Compression
- Document Clustering
- Recommendation Systems

---

# 2. Hierarchical Clustering

## What is Hierarchical Clustering?

Hierarchical Clustering builds a hierarchy of clusters using a tree-like structure called a **Dendrogram**. Unlike K-Means, it does not require specifying the number of clusters beforehand.

---

## Types

### Agglomerative Clustering (Bottom-Up)

- Each data point starts as its own cluster.
- The closest clusters are merged repeatedly.
- The process continues until all points belong to one cluster.

---

### Divisive Clustering (Top-Down)

- All data points begin in one cluster.
- The cluster is recursively divided into smaller clusters.

---

## Agglomerative Clustering Steps

1. Treat every data point as a separate cluster.
2. Compute pairwise distances.
3. Merge the two closest clusters.
4. Update the distance matrix.
5. Repeat until one cluster remains.

---

## Linkage Methods

- **Single Linkage** – Minimum distance
- **Complete Linkage** – Maximum distance
- **Average Linkage** – Average distance
- **Ward Linkage** – Minimizes within-cluster variance

---

## Dendrogram

A dendrogram visually represents how clusters are merged. Cutting the dendrogram at a selected height determines the final number of clusters.

---

## Advantages

- No need to specify K initially
- Produces an interpretable dendrogram
- Suitable for small datasets
- Captures hierarchical relationships

---
