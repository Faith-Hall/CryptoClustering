# CryptoClustering
In this challenge, you’ll use your knowledge of Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.
---
- load the data into a Pandas DataFrame
- generate summary stats
- line plot the data:
  
![Screenshot 2023-11-12 104723](https://github.com/Faith-Hall/CryptoClustering/assets/135525815/0a1a5a12-6778-4c24-90cd-e16454cfc225)
---
### Prepare the Data
- use the `StandardScaler()` module from scikit-learn to normalize the data from the CSV file
- create dataframe with the scaled data
- set the coinid column as index
---
### Find the Best Value for k Using the Original Scaled DataFrame
- create a list with the number of k-values from 1-11
- create a loop to compute hte inertia with each possible value of k
```
for i in k:
    k_model = KMeans(n_clusters=i, random_state=1)
    k_model.fit(market_data_transformed)
    inertia_1.append(k_model.inertia_)
```
- create a dictionary with the data to plot the elbow curve
- plot the line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k:

![Screenshot 2023-11-12 105200](https://github.com/Faith-Hall/CryptoClustering/assets/135525815/cb451ac4-8b8a-49a8-95d7-2a42e0c6074d)
---
### Cluster Cryptocurrencies with K-means Using the Original Scaled Data
---
### Optimize Clusters with Principal Component Analysis
---
### Find the Best Value for k Using the PCA Data
---
### Cluster Cryptocurrencies with K-means Using the PCA Data





