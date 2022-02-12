# Implementation of K-Means Clustering Algorithm
## Aim
To write a python program to implement K-Means Clustering Algorithm.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation

## Algorithm:

### Step1
<br>Import pandas and matplotlib.pyplot

### Step2
<br>Import KMeans from sklearn package

### Step3
<br>Read the csv fileusing df.head() and assign it to the variables

### Step4
<br>Find the centroid using KMeans

### Step5
<br>Run the program and predict the output

## Program:
```
##Program Developed by : K.Balaji
## Reference number : 21005757
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
import seaborn as sns
import warnings
warnings.filterwarnings('ignore')
X1 = pd.read_csv('clustering.csv')
print(X1.head(2))
X2 = X1.loc[:, ['ApplicantIncome', 'LoanAmount']]
print(X2.head(2))
X = X2.values
sns.scatterplot(X[:,0], X[:, 1])
plt.xlabel('Income')
plt.ylabel('Loan')
plt.show()
kmean=KMeans(n_clusters=4)
kmean.fit(X)
print('Cluster Centers:', kmean.cluster_centers_)
print('Labels:', kmean.labels_)
predicted_class = kmean.predict([[9000,120]])
print('The cluster group for Applicant Income 9000 and Loanamount 120')





```
## Output:

### Insert your output
![output](./1.png)
![output](./2.png)
![output](./3.png)
<br>

## Result
Thus the K-means clustering algorithm is implemented and predicted the cluster class using python program.