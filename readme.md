# Clustering Analysis: K-Means vs DBSCAN

## Introduction

This project involves clustering analysis using K-Means and DBSCAN algorithms to segment data effectively. The goal is to compare the performance of these clustering algorithms using the Elbow Method for K-Means and evaluate the results of DBSCAN. This analysis was part of a project for a certification from Matbakhonneh.

**Note:** Due to licensing restrictions, the actual dataset used cannot be shared. However, the methodologies and results are discussed in detail below.

## Exploratory Data Analysis (EDA)

Before applying clustering algorithms, we performed Exploratory Data Analysis (EDA) to understand the dataset's structure and characteristics. The key steps included:

1. **Loading and Inspecting Data**
    - Loaded the dataset into a DataFrame.
    - Checked for missing values and data types.

2. **Summary Statistics**
    - Calculated basic statistics such as mean, median, and standard deviation for numerical features.

3. **Feature Visualization**
    - Plotted histograms and box plots to visualize the distribution of features.

## Clustering Algorithms

### K-Means Clustering

K-Means clustering is a popular partitioning method that divides the data into `k` clusters based on feature similarity. The algorithm iteratively refines cluster centroids to minimize the within-cluster variance.

#### Elbow Method for Optimal `k`

To determine the optimal number of clusters (`k`), we used the Elbow Method. This involves plotting the sum of squared distances from each point to its assigned cluster center (inertia) against different values of `k`.

**Steps:**
1. **Compute K-Means for Different `k` Values**
2. **Plot the Inertia vs. `k`**
3. **Identify the Elbow Point**

#### Results

```python
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans

# Sample code to determine the optimal k using the Elbow Method
inertia = []
k_range = range(1, 11)

for k in k_range:
    kmeans = KMeans(n_clusters=k,
