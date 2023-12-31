# CryptoClustering

# Overview
The Crypto Clustering project aims to predict if cryptocurrencies are affected by 24-hour or 7-day price changes using unsupervised learning techniques, specifically K-means clustering. Additionally, the project explores the impact of dimensionality reduction using Principal Component Analysis (PCA) on clustering.

# Steps
1. Load and preprocess the data.
2. Scale the data using StandardScaler.
3. Find the best value for k using the elbow method.
4. Cluster cryptocurrencies with K-means using the original scaled data.
5. Perform PCA to reduce the features to three principal components.
6. Find the best value for k using the PCA data.
7. Cluster cryptocurrencies with K-means using the PCA data.
8. Visualize and compare the results using hvPlot.

# Findings
Original Data:

![Original_Cryto_Returns](https://github.com/snbadeaux/CryptoClustering/assets/134640833/be490694-6e59-426a-beba-fae4584d1c72)


Elbow Curve Comparison:

![Scaled Elbow Curve](https://github.com/snbadeaux/CryptoClustering/assets/134640833/7199b3e0-e6f7-4279-962f-422a6b824b1f)

![PCA_Elbow_Curve](https://github.com/snbadeaux/CryptoClustering/assets/134640833/4f15fb12-92db-45c3-9256-d2825dfdb75e)

Both curves show that k=4 is ideal but, the elbow curve for the PCA data (elbow curve 2) shows a lower inertia value compared to the elbow curve for the original data (elbow curve 1). This indicates that using fewer features resulted in a reduction in the sum of squared distances within the clusters. A lower inertia value suggests better clustering performance and tighter grouping of data points within each cluster.<br><br>



Scatter Plot Cluster Comparison:

![Scatter_Plot_by_KMeans_Segments](https://github.com/snbadeaux/CryptoClustering/assets/134640833/7d991a68-2fc9-4363-b5de-2aed91ac9e93)

![PCA_Scatter_Plot_by_KMeans_Segments](https://github.com/snbadeaux/CryptoClustering/assets/134640833/257826f6-69b3-4fc4-b5be-1e53ebebeb64)

Scaled Data Cluster Graph 1: The clusters are overlapping, and there is no clear separation or distinct clusters. This suggests that using the original data, with more features, may not have effectively captured the underlying patterns or structure of the data for clustering purposes.<br>

PCA Cluster Data Graph 2: The clusters in this graph are not overlapping, and there is a clear separation and well-defined clusters. You can identify 4 distinct clusters. This indicates that using fewer features, through Principle Component Analysis, has potentially reduced noise and helped reveal more distinct patterns in the data, leading to more meaningful and separable clusters.<br><br>

# Conclusion
Based on these observations, it seems that using fewer features (PCA data) to cluster the cryptocurrency data using K-Means has had a positive impact. It has resulted in better-defined and separable clusters compared to using the original data. The reduction in the number of features through PCA has likely helped to highlight the essential patterns and reduce the impact of noise, leading to more accurate and meaningful clustering results.

# Sources
hvPlot: https://hvplot.holoviz.org/ <br>
Stack Overflow: https://stackoverflow.com/
