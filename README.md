# Unsupervised Learning: Clustering

A hands-on notebook covering two core clustering algorithms — **K-Means** and **DBSCAN** — implemented from scratch using `scikit-learn` on synthetic datasets.

![Clustering Preview](assets/clustering_preview.png)

## Overview

Unsupervised learning trains on data with no labels — the goal is to find natural structure or groupings in the data on its own. This notebook walks through two widely used clustering algorithms, how they work, and when to use one over the other.

## Algorithms Covered

### K-Means
Partitions data into a fixed number of clusters (`K`) by minimizing distance between points and their cluster center.
- Dataset: `make_blobs` (700 samples, 2 centers)
- Optimal `K` selected using the **Elbow Method**
- Best suited for round, evenly distributed clusters

### DBSCAN
Groups points based on density rather than distance to a center, and automatically detects outliers.
- Dataset: `make_moons` (500 samples, non-linear shapes)
- Parameters: `eps = 0.2`, `min_samples = 5`
- Best suited for irregular, non-convex cluster shapes and noisy data

## Workflow

1. Generate / load dataset
2. Scale features with `StandardScaler`
3. Select model parameters (K via elbow method / eps & min_samples for DBSCAN)
4. Fit model and assign cluster labels
5. Visualize results with scatter plots
6. Compare and conclude
