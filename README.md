# BDA Lab – K-Means Clustering Assignment

This repository contains the dataset and starter code for the **K-Means Clustering Lab Exercise**.

## Objective

Perform clustering on customer data using **K-Means algorithm** and visualize the clusters.

## Dataset

customers_large_dataset.csv

Columns used:

* AnnualIncome
* SpendingScore

## Program Steps

1. Load dataset using pandas
2. Select required columns
3. Apply K-Means clustering
4. Plot clusters using matplotlib

## Submission Instructions

### Step 1 – Fork Repository

Click **Fork** on the top-right of this repository.

### Step 2 – Clone Repository

```
git clone https://github.com/YOUR-USERNAME/BDA-KMeans-Clustering-Lab.git
```

### Step 3 – Create Submission Folder

Inside the `submissions` folder create a folder:

```
submissions/YourName_RegisterNumber
```

Example:

```
submissions/Ravi_21CS101
```

### Step 4 – Upload Files

Upload:

* Python code
* Output screenshot

Example:

```
submissions/Ravi_21CS101/kmeans.py
submissions/Ravi_21CS101/output.png
```

### Step 5 – Push and Create Pull Request

```
git add .
git commit -m "KMeans Lab Submission"
git push origin main
```

Then create a **Pull Request**.

### Program:
```
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans

```
```
data = pd.read_csv("C:\\Users\\admin\\Downloads\\customers_large_dataset.csv")
X = data[["AnnualIncome", "SpendingScore"]]
k = 3 
kmeans = KMeans(n_clusters=k, random_state=42)
kmeans.fit(X)
```
```
labels = kmeans.labels_
plt.figure()
plt.scatter(X["AnnualIncome"], X["SpendingScore"], c=labels)

centers = kmeans.cluster_centers_
plt.scatter(centers[:, 0], centers[:, 1], marker='X', s=200)
plt.xlabel("Annual Income")
plt.ylabel("Spending Score")
plt.title("K-Means Clustering")
plt.show()
```


### Output:

<img width="1108" height="138" alt="image" src="https://github.com/user-attachments/assets/8cae4746-a00c-4527-b080-aa4095d2756f" />

<img width="1023" height="641" alt="image" src="https://github.com/user-attachments/assets/a9e3914b-51f1-43f3-a941-afd48be65de9" />

<img width="945" height="688" alt="image" src="https://github.com/user-attachments/assets/7bf5bd6b-bdd7-4dfe-9fc5-76f2ec5ed646" />





## Important Rules

* Do not edit other folders
* Upload only inside your folder
* Follow naming format
