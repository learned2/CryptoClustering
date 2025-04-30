# CryptoClustering
# CryptoClustering

## Overview

The **CryptoClustering** project applies unsupervised machine learning techniques to explore how cryptocurrencies group based on their short-term price movements. By using K-Means clustering and Principal Component Analysis (PCA), this project identifies natural clusters among cryptocurrencies using 24-hour and 7-day price change data. This analysis offers insight into patterns of volatility and correlation in the crypto market.

## Objectives

- Normalize cryptocurrency price change data using `StandardScaler`
- Use K-Means clustering to segment cryptocurrencies
- Apply the Elbow Method to identify the optimal number of clusters
- Visualize clusters in both raw and PCA-reduced feature spaces
- Evaluate the impact of dimensionality reduction on clustering results

## Technologies Used

- Python
- Pandas
- scikit-learn
- hvPlot
- Jupyter Notebook

## Files

- `Crypto_Clustering.ipynb`: Main notebook with code and analysis
- `crypto_market_data.csv`: Source dataset containing cryptocurrency price changes
- `README.md`: Project summary and instructions

## Methodology

1. **Data Preparation**
   - Loaded historical 24-hour and 7-day price change data for various cryptocurrencies
   - Scaled features using `StandardScaler`

2. **K-Means Clustering (Raw Features)**
   - Applied the Elbow Method to determine the optimal number of clusters
   - Clustered the scaled data using K-Means
   - Visualized clusters using a scatter plot

3. **Dimensionality Reduction with PCA**
   - Reduced data from two features to two principal components
   - Reapplied K-Means and the Elbow Method
   - Visualized new clusters in PCA space

4. **Comparison and Evaluation**
   - Compared Elbow curves and cluster visualizations before and after PCA
   - Analyzed trade-offs in interpretability and cluster separation

## Results

- Optimal `k` found to be 5 using raw features and 4 using PCA-reduced data
- PCA preserved nearly 100% of the original variance
- Clusters in PCA space were visually more distinct
- Reduction to fewer features simplified visualization but reduced direct interpretability

## Conclusion

This project demonstrates how unsupervised learning and dimensionality reduction can uncover meaningful patterns in financial data. While PCA simplifies clustering, it abstracts the relationship between the input features and the resulting groupings. Such trade-offs must be considered when choosing clustering strategies in real-world applications.
