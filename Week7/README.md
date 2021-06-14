# Week7:<br>

With supervised learning, the performance of many supervised learning algorithms will be pretty similar, and what matters less often will be whether you use learning algorithm a or learning algorithm b, but what matters more will often be things like the amount of data you create these algorithms on, as well as your skill in applying these algorithms. Things like your choice of the features you design to give to the learning algorithms, and how you choose the regularization parameter etc.<br>

SVM sometimes gives a cleaner, and sometimes more powerful way of learning complex non-linear functions.<br>

SVM acts as a large margin classifier, separates/classifies data with a large margin and this is because of the optimization problem. The decision boundary has some larger minimum distance from all training examples. **This happens only when C is large. i.e. SVM acts as a large-margin classifier only when C is large**<br>

If all you're doing is use a large margin classifier then your learning algorithms can be sensitive to outliers. However, Support Vector Machines do a better job in ignoring the outliers.

Regularization parameter C in SVMs:
C -> Very Large -> less regularization, chances of high variance, over fitting<br>
<br>
C plays a role very similar to (1/Lambda)<br>
C ~ 1/Lambda

## SVM Decision Boundary:

the decision boundary is Theta' . X
i.e. th0 + th1.x1 + th2.x2 = 0
slope = - th1/th2

slope of theta vector = th2/th1

Therefore, decision boundary is perpendicular to the theta vector.

## Kernels:
In the abstract these different similarity functions are called kernels and we can have different similarity functions and the specific example given here is called the Gaussian kernel.<br>

When we decrease sigma, the countour plot becomes narrower i.e. the feature falls to zero much more rapidly.<br>
If we increase sigma, the countour plot becomes broader. i.e. the feature falls to zero much more slowly.
<br>

We can achieve complex non-linear decision boundaries with kernels.<br>
Kernels in logistic regression run very slowly and hence we use Kernels only with SVMs because of the computational tricks that come with it.

<br>

We choose parameters that peform the best on the cross-validation data.