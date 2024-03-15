# Project Goal:

* This project aims to group cryptocurrencies into clusters based on their price changes in different timeframes (24 hours and 7 days) using an unsupervised machine learning technique called K-Means Clustering.

## Data:
* The project utilizes a CSV file named "crypto_market_data.csv" containing price change data for various cryptocurrencies.

## Process:

1. ### Import and Analyze Data:
  * First step is to import the CSV data into a pandas DataFrame.
  * After importing the data, it's time to do some exploratory data analysis using summary statistics and visualizations with HvPlot to understand its characteristics.

2. ### Data Preprocessing:
  * The data is then normalized using scikit-learn's StandardScaler to ensure features are on a similar scale before applying K-means clustering.

3. ### Finding the Optimal Number of Clusters (k):
  * To start the process of using this technique, we start with a method known as the "elbow method" which determines the ideal number of clusters (k) for K-means.
  * The elbow method involves calculating the inertia (a measure of how spread out the data points are within a cluster) for different values of k and plotting them. The optimal k is usually chosen when the line in the chart starts to plateau or bend (the "elbow" of the curve).
  
4. ### Clustering with K-means (Original Data):
  * Once the optimal k is found, the script uses K-means clustering to group the cryptocurrencies into k clusters based on their price changes.
  * The script will then create a scatter plot visualizing the clusters using price changes over different timeframes.
  * The data points are colored coded according to their assigned cluster so you know which point reveals the corresponding cryptocurrency name.

5. ### Optimizing Clusters with Principal Component Analysis (PCA):
  * After fitting the model and testing, We use PCA to improve the clustering by removing the most irrelevant features/columns within the scatter plot.
  * PCA also helps find the features/columns with the most variance which can be significant when looking at the crypto names.
  * Once PCA is established, we will have a good understanding of what features impact the price change the most within the crypto names.

6. ### Using PCA data with clustering:
  * In this step I used the PCA data with the K-means clustering technique with the chosen k(4) to group the cryptocurrencies based on the principal components.

7. ### Comparing Results with and without PCA:
* To compare the clustering effectiveness, I created visualizations contrasting the results with and without PCA:
  * One visualization compared the elbow curves used to determine the optimal k in both scenarios (original data vs. PCA data).
  * Another visualization compared the scatter plots of the final clusters using the original data and the PCA data.

## Impact of Using Fewer Features:
* By visually analyzing the comparisons, you will observed that using fewer features (principal components) result in clusters more spread out and easier to interpret due to the reduced number of columns used.
