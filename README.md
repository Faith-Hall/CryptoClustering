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
- initialize the K-Means model using the best value for k
- fit the K-Means model using the scaled data
- predict the clusters to group the cryptocurrencies using the scaled data
- create a copy of the dataframe
- display the data in a scatter plot:

 ![Screenshot 2023-11-12 105410](https://github.com/Faith-Hall/CryptoClustering/assets/135525815/eddc2d9f-6d05-404b-8916-4d9b43b82eb8)
---
### Optimize Clusters with Principal Component Analysis
- create a pca model instance
- fit and transform the model to reduce to three principal components
- find the total variance of the three principal components: 0.8844285111826466
- create a new dataframe with the PCA data
  
---
### Find the Best Value for k Using the PCA Data
- create a list with the number of k-values from 1-11
- create a loop to compute hte inertia with each possible value of k
```
for i in k:
    k_model = KMeans(n_clusters=i, random_state=1)
    k_model.fit(cluster_pca_df)
    inertia_2.append(k_model.inertia_)
```
- create a dictionary with the data to plot the elbow curve
- plot the line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k:

![Screenshot 2023-11-12 105848](https://github.com/Faith-Hall/CryptoClustering/assets/135525815/b4e480f3-4445-4a70-9a1c-d8a5cad29bd1)
---
### Cluster Cryptocurrencies with K-means Using the PCA Data
- initialize the K-Means model using the best value for k
- fit the K-Means model using the PCA data
- predict the clusters to group the cryptocurrencies using the scaled data
- create a copy of the dataframe
- display the data in a scatter plot:
![Screenshot 2023-11-12 110008](https://github.com/Faith-Hall/CryptoClustering/assets/135525815/ea41b894-061b-45aa-9364-f2d591dca981)

## Visualize and Compare the Results 
![Screenshot 2023-11-12 110059](https://github.com/Faith-Hall/CryptoClustering/assets/135525815/2c2f3149-3036-409c-8dc7-925c4b26ad70)







