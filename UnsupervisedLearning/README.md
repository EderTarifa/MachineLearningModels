# Project: Preprocessing and Clustering Techniques

## Overview

This project applies various preprocessing and clustering techniques to a dataset of fruit instances. The dataset includes features such as weight, length, width, and symmetry, with an additional categorical variable representing the cleft size of the fruit. The project focuses on preparing the data for clustering analysis and evaluates the performance of two clustering algorithms: Hierarchical Clustering and KMeans.

## Preprocessing

Several preprocessing steps are applied to the data to ensure its suitability for clustering:

- **Imputation of Missing Values**: Missing data is handled using advanced imputation techniques.
- **Encoding of Cleft Variable**: The categorical cleft size variable is encoded numerically for analysis.
- **Outlier Removal**: Extreme outliers are identified and treated to improve data quality.
- **Scaling**: The variables are scaled using different techniques to standardize the data range.

## Clustering Techniques

### Hierarchical Clustering

Hierarchical Clustering is applied to the preprocessed data, with different linkage methods (single, average, ward, complete) and dissimilarity measures (Euclidean, Manhattan, Chebyshev, correlation) tested to find the best clustering solution.

### KMeans Clustering

The KMeans algorithm is used to determine the optimal number of clusters. Evaluation is performed using the Silhouette coefficient and inertia metrics, which help identify the best model based on clustering performance.

## Evaluation

- **Hierarchical Clustering Evaluation**: The performance of Hierarchical Clustering is evaluated using the silhouette coefficient for different linkage methods and dissimilarity measures.
- **KMeans Clustering Evaluation**: KMeans clustering is evaluated using the Silhouette coefficient and inertia to determine the optimal number of clusters and the best scaling method.

## Conclusion

The project concludes with a comparison of the best clustering models, highlighting the most influential variables for each cluster. The KMeans model with robust scaling achieved the highest silhouette coefficient, while Hierarchical Clustering also provided good results, making it a viable alternative.
