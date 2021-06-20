# Week9: <br>

## Anomaly Detection:
1. Training set consists of only negative examples. Cross-validation and test sets will have some positive examples.
2. **Error Analysis:** Look at the anomaly that the algorithm is failing to flag, and see if that inspires you to create some new feature. E.g. So find something unusual about that aircraft engine and use that to create a new feature, so that with this new feature it becomes easier to distinguish the anomalies from your good examples.
3. Calculating inverese of a large nxn matrix is computationally expensive.
4. In multivariate gaussian distribution, for the covariance matrix(sigma) to be invertible, the conditions are:<br>
   1. m>=10n (recommended, otherwise m>=n)
   2. No redundant features i.e.features that are linearly dependant e.g x3 = x1+x2, x3=x2
5. The original model p(x1;mu1;sigma1^2)x..x..p(xn,mun,sigman^2) corresponds to a multivariate Gaussian where the contours of p(x,mu,Sigma) are axis alligned.
6. The multivariate gaussian model can automatically capture correlaations between different features in x.
7. The original model can be more computationally efficient that the multivariate gaussian model, and thus might scale better to very large values of n(number of features).
8. In the case where a user has given no ratings for any movie, the recommender system will give an output rating of zero for every movie. This is because, for minimizing the cost function the first term of Theta'*X will be zero as it is computed only for r(i,j)=1. So, only the regularization term remains for cost minimization and that leads to Theta being [0 0 0 ..0] for the new user. Hence, all predicted ratings will be zero. To prevent this, we use mean normalization.