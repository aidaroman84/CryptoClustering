# CryptoClustering

## Overview
In this challenge, I will use my knowledge of Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

## Instructions

1. Prepare the Data
2. Find the Best Value for k Using the Original Scaled DataFrame
3. Cluster Cryptocurrencies with K-means Using the Original Scaled Data
4. Optimize Clusters with Principal Component Analysis
5. Find the Best Value for k Using the PCA Data
6. Cluster Cryptocurrencies with K-means Using the PCA Data
7. Create composite plot to Visualize and Compare the Results

## Results

1. Prepare the Data

![scaled_dataframe](https://github.com/aidaroman84/CryptoClustering/blob/main/Images/Scaled%20DataFrame.png)

2. Find the Best Value for k Using the Original Scaled DataFrame
   
   Based on the visual inspection of the elbow curve, the best value for k is 4.

![elbow_original](https://github.com/aidaroman84/CryptoClustering/blob/main/Images/Elbow%20Curve%20Original.png)

3. Cluster Cryptocurrencies with K-means Using the Original Scaled Data
   
![cluster_original](https://github.com/aidaroman84/CryptoClustering/blob/main/Images/Cluster%20Plot%20Original.png)

4. Optimize Clusters with Principal Component Analysis

   The three principal components together explain about 89.50% of the variance in the dataset.

![PCA_Components](https://github.com/aidaroman84/CryptoClustering/blob/main/Images/PCA%20components.png)

5. Find the Best Value for k Using the PCA Data

   The best value for k when using the PCA-transformed data is 4.
   Comparing this case to the best k value found using the original data, which was also 4, we can see that the best value for k does not differ when using the PCA data.

![elbow_PCA](https://github.com/aidaroman84/CryptoClustering/blob/main/Images/Elbow%20Curve%20PCA.png) 

6. Cluster Cryptocurrencies with K-means Using the PCA Data

![cluster_PCA](https://github.com/aidaroman84/CryptoClustering/blob/main/Images/Cluster%20Plot%20PCA.png) 

7. Create composite plot to Visualize and Compare the Results

 * Elbow Curves Comparison:
The elbow curves for both original and PCA data do not show a drastically different shape around k=4, suggesting that the choice of k is consistent regardless of the feature reduction. However, the lower inertia for the PCA curve at the same k value indicates more efficient clustering after feature reduction.

 * Visual Analysis of Clusters:
The scatter plot of the original data shows a wider spread of clusters, which indicates a higher variability within clusters. The points are not as tightly grouped, and the clusters may overlap more. The PCA scatter plot presents clusters that are more clearly defined and separated. The points within each cluster are closer to each other, and there is less overlap between clusters. This can indicate that PCA has helped to emphasize the most important variances that define the clusters.

 * Conclusion:
Using PCA for dimensionality reduction before applying K-Means clustering seems to have a positive impact on the clustering results. It leads to a lower inertia at k=4, indicating that the clusters are more cohesive and better separated. Even though the optimal number of clusters doesn't change with PCA, the clusters formed using PCA features are tighter, which might result in more reliable and interpretable groupings in the context of the data being analyzed.This impact is a direct result of PCA's ability to capture the most significant features that contribute to the data's variance, thereby enhancing the clustering process.

