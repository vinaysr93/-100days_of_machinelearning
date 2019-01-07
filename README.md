# -100days_of_machinelearning
Taking up 100 days of macine learning challenge and documenting my work.


Day 1-7/1/19

Since I had already started with Introduction to machine learning before... I am continuing my journey. Today I've learnt about K means algorithm. Did some quizzes on the same. 

Below are my notes for the same.

Unsupervised Learning 

Clustering:

Most basic algorithm is K means 

K means works in two steps:
Assign 
Optimize
One of the parameter that needs to be defined for k means is the number of clusters.

Parameters for K mean:

N clusters- Default value for n_clusters is 8
Max_iter- Number of iterations of the algorithms you want to go through-300
N_init- Number of initializations.


K Means Limitations:

K means is what is called a hill climbing algorithm and is dependent on where you initially put your cluster centres.


K Means Syntax

from sklearn.cluster import KMeans
import numpy as np
X = np.array([[1, 2], [1, 4], [1, 0],[4, 2], [4, 4], [4, 0]])
kmeans = KMeans(n_clusters=2, random_state=0).fit(X)
kmeans.labels_
array([0, 0, 0, 1, 1, 1], dtype=int32)
kmeans.predict([[0, 0], [4, 4]])
array([0, 1], dtype=int32)
kmeans.cluster_centers_array([[1., 2.],[4., 2.]])
