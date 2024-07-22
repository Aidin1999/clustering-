# Clustering Analysis: K-Means vs DBSCAN

## Introduction

In this project, we explored clustering techniques using K-Means and DBSCAN algorithms to segment data. The aim was to compare these algorithms and evaluate their performance using various metrics. This analysis was conducted as part of a certification project from Matbakhonneh. Due to licensing restrictions, the actual dataset cannot be shared.

## Exploratory Data Analysis (EDA)

Before applying clustering algorithms, an exploratory data analysis (EDA) was performed to understand the dataset's characteristics. This involved:

1. **Data Inspection**: Examining the dataset for completeness, checking for missing values, and understanding the data types.
2. **Summary Statistics**: Computing basic statistics such as mean, median, and standard deviation to summarize the numerical features.
3. **Feature Visualization**: Visualizing feature distributions using histograms and box plots to get an initial understanding of the data spread and outliers.

## Clustering Algorithms

### K-Means Clustering

K-Means is a popular clustering algorithm that partitions data into `k` distinct clusters. It works by:

1. **Initialization**: Selecting `k` initial centroids (cluster centers) randomly.
2. **Assignment**: Assigning each data point to the nearest centroid, forming clusters.
3. **Update**: Recalculating centroids as the mean of all data points in each cluster.
4. **Iteration**: Repeating the assignment and update steps until centroids stabilize.

**Elbow Method**:
To determine the optimal number of clusters (`k`), the Elbow Method is used. This involves plotting the sum of squared distances from each point to its assigned centroid (inertia) for different values of `k` and identifying the "elbow" point where the rate of decrease sharply changes. This point suggests the optimal `k`.

### DBSCAN Clustering

DBSCAN (Density-Based Spatial Clustering of Applications with Noise) is a density-based algorithm that identifies clusters based on the density of data points. It works by:

1. **Defining Neighborhood**: Using parameters `eps` (maximum distance between points) and `min_samples` (minimum number of points required to form a cluster).
2. **Core Points**: Identifying points that have at least `min_samples` within `eps`.
3. **Cluster Formation**: Expanding clusters from core points and merging them based on density. Points that do not meet the criteria are labeled as noise.

**Parameter Selection**:
Choosing appropriate `eps` and `min_samples` is crucial for DBSCAN. These parameters can significantly affect the clustering results and the identification of noise.

## Comparison and Evaluation

### Performance Metrics

- **K-Means**:
  - **Inertia**: Measures the sum of squared distances between points and their respective centroids. Lower inertia values indicate better clustering quality.
  - **Cluster Centers**: The final centroids are used to interpret the center of each cluster.

- **DBSCAN**:
  - **Number of Clusters**: Indicates the number of clusters identified by the algorithm, including noise points.
  - **Cluster Sizes**: Provides insight into the distribution of points within each cluster.
  - **Noise Points**: DBSCAN identifies and reports noise points that do not belong to any cluster.

### Visualization

**K-Means Visualization**:
The clusters formed by K-Means can be visualized by plotting data points colored by their cluster assignments. Cluster centroids are often highlighted to show the center of each cluster.

**DBSCAN Visualization**:
DBSCAN clusters are visualized by plotting data points colored according to their cluster assignments, including noise points which are typically marked differently.

## Conclusion

- **K-Means**: Effective when the number of clusters is known in advance and clusters are expected to be spherical. It provides clear cluster centroids and is sensitive to initial centroid placement.

- **DBSCAN**: Useful for data with noise and clusters of varying shapes and sizes. It does not require specifying the number of clusters beforehand but is sensitive to parameter selection.

The choice of clustering algorithm depends on the nature of the data and the specific requirements of the analysis. Both K-Means and DBSCAN offer valuable insights and have their own strengths and limitations.

---

**Project by:** Aidin Miralmasi

**Certificate:** Matbakhonneh
