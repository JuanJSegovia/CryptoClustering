# CryptoClustering: Unsupervised Learning of Cryptocurrency Behavior

## Overview of the Analysis
The purpose of this analysis is to apply unsupervised machine learning techniques to cluster cryptocurrencies based on their 24-hour and 7-day price changes. By identifying patterns and groupings, the company can better understand market dynamics and make informed decisions. This project uses clustering with K-Means and dimensionality reduction with Principal Component Analysis (PCA) to explore the data.

### Methodology
Data Preparation:

The cryptocurrency data was loaded from crypto_market_data.csv into a pandas DataFrame.
Data was normalized using the StandardScaler() module from scikit-learn.
The "coin_id" column was set as the index for easy reference. The elbow method was applied to the scaled data to find the optimal number of clusters (k) for K-Means. The K-Means algorithm was applied to cluster the cryptocurrencies into distinct groups based on the optimal value of k.

### Dimensionality Reduction with PCA:

PCA was used to reduce the data to three principal components, capturing the majority of the variance.
The elbow method was re-applied to the PCA-reduced data to determine if the optimal value of k changed.
Visualization:

Scatter plots of clusters were created using hvPlot for both the original scaled data and the PCA-reduced data.
Composite plots compared the elbow curves and cluster visualizations.
Results
Optimal k (original scaled data): k=3
Optimal k (PCA-reduced data): k=4
Explained Variance (PCA): [0.3719856 , 0.34700813, 0.17603793]

### Key Observations:
Clustering results from the original scaled data and PCA-reduced data were compared.
The total explained variance of the three principal components indicated how much information was preserved.
Using PCA reduced the dimensionality while maintaining interpretability and clustering accuracy.
Analysis of Clustering Results
Impact of Using PCA:
Reducing the features with PCA simplifies the data without significantly affecting clustering performance. However, subtle changes in the optimal number of clusters (k) or the cluster boundaries may occur, depending on the explained variance.

### Recommendations:
The clustering results provide actionable insights into cryptocurrency behavior based on price changes. If fewer features are needed for analysis, PCA offers a streamlined approach while retaining most of the information.
