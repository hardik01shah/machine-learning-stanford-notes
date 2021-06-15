# Week 8:

>Unsupervised Learning:<br>
Find some structure in unlabeled data in the training set given to you.

e.g. clustering algorithms

Clustering examples:
1. Coherent groups of friends
2. Reorganize resources in computing
3. market segmentation<br>

K-Means ALgorithm:<br>
1. Randomly initialize two points called cluster centroids(bcoz we want to classify the data into 2 clusters)<br>
2. K-Means is an iterative algorithm.<br>
3. Two steps now, cluster assignment step, and second is a move centroid step.
4. Cluster Assignment:<br>
    Assign each sample to the closer cluster centroid.<br>
5. Move Centroid:<br>
    Move the cluster centroids to the mean of each cluster.<br> 
6. Continue this iteratively  <br>

c(i) = minimize over k ||x(i) - mu(k)||^2,
where mu(k) is a cluster centroid.<br>
<br>
The Cluster assignment step minimizes the cost function keeping the cluster centroids fixed and changing cluster assignment to minimize the cost i.e. minimize the cost by changing c(1), c(2)...c(m) keeping mu(1), mu(2).....mu(k) fixed.<br>

The move centroid step minimizes the cost function keeping the cluster assignment fixed and changing the cluster centorids i.e. minimize the cost by changing mu(1), mu(2).....mu(k) keeping c(1), c(2)...c(m) fixed.
<br>
<br>

>Random Initialization:<br>
should have k < m<br> 
Randomly pick K training examples and set mu1, mu2,..muk as the selected K examples.

*K-means can end up converging to different solutions depending on exactly how the clusters were initialized, and can end up at local optimum.*
<br>

Try multiple random initializations for finding the best global optima for K means.<br>
Random initialization can make a huge difference when the number of clusters is small i.e. 2-10. If the number of clusters is large ~100, random initialization may give a slightly better solution but not much difference. It is most likely bound to give a decent clustering in the first initialization.<br>

Elbow Method(for deciding K):<br>
Look for an elbow joint in the graph of cost function v/s K(no. of clusters) graph.

Principal Component Analysis for dimensionality reduction(PCA):<br>
1. Use feature scaling so that the values of features are in a comparable range.
2. PCA is different from linear regression. Linear regression aims to minimize yhat(i) - y(i), whereas PCA aims to minimize pependicular distance of y(i) from the hypothesis. Also, there is no special variable y that we are trying to predict in PCA. They are very different algos.
3. Vectorized implementation of covariance matrix:
   Sigma = (1/m)\*X'*X;
4. Suppose z belong to R(k) is to be found from X belong to R(n):
   1. Sigma = (1/m)\*X'*X;
   2. [U,S,V] = svd/eig(Sigma)
   3. Ureduce = U(:,1:k)
   4. z = Ureduce'*x
5. Reconstruction from compressed representation:
   Xapprox = Ureduce*Z
6. To choose optimal k(no. of principal components), run svd only once. You don't need to run it for every k you check.
7. We can visualize data only for k=2 or k=3 features, so we can use PCA for visualization.
8. Also we can spped up learning algorithm by reducing the number of features. Here the number of features is decided by % of variance retained.
9. PCA may throw away valuable information if used for the purpose of preventing overfitting because it does not take into account the values of y. PCA is a bad method for addressing overfitting. Use regularization instead.