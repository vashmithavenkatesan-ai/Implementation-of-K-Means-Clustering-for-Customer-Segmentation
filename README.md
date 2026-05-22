# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries and create the customer dataset.
2. Select the data and apply the K-Means algorithm.
3. Train the model using fit() method.
4. Display the cluster labels for customer segmentation.

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: VASHMITHA V
RegisterNumber:  212225240180
# Implementation of K-Means Clustering for Customer Segmentation

# Import libraries
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans

# Sample customer data
# Annual Income and Spending Score

data = {
    'Annual_Income': [15,16,17,18,19,20,21,22,23,24,
                      60,62,64,65,66,67,68,69,70,72],

    'Spending_Score': [39,81,6,77,40,76,6,94,3,72,
                       55,52,59,51,50,48,47,46,45,44]
}

# Create DataFrame
df = pd.DataFrame(data)

print("Customer Data")
print(df)

# Select features
X = df[['Annual_Income', 'Spending_Score']]

# Apply K-Means Clustering
kmeans = KMeans(n_clusters=3, random_state=0)

# Fit the model
kmeans.fit(X)

# Predict clusters
df['Cluster'] = kmeans.labels_

print("\nCustomer Segments")
print(df)

# Plot the clusters
plt.scatter(X['Annual_Income'],
            X['Spending_Score'],
            c=df['Cluster'])

# Plot centroids
plt.scatter(kmeans.cluster_centers_[:,0],
            kmeans.cluster_centers_[:,1],
            s=200,
            marker='X')

# Labels
plt.xlabel("Annual Income")
plt.ylabel("Spending Score")

plt.title("K-Means Clustering for Customer Segmentation")

# Show graph
plt.show()
*/
```

## Output:

<img width="612" height="743" alt="Screenshot 2026-05-22 113552" src="https://github.com/user-attachments/assets/842c0582-5b45-41b0-9968-ac2bdd227ffb" />
<img width="720" height="456" alt="Screenshot 2026-05-22 113603" src="https://github.com/user-attachments/assets/9f7eda43-6104-4d17-b316-76052c055e18" />


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
