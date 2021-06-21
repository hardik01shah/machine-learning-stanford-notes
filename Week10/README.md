# Week10:

## Training on Large DataSets:
1. If a training set of large size is available, first train the model on a small subset of the dataset and check if the model gives high variance(overfitting). If it does, using more data is likely to improve the performance of the algorithm.
2. The gradient descent in the initial weeks was called *Batch Gradient Descent* because we were loooking at all the training examples at a time.
3. Stochastic Gradient Descent takes a small learning step just by looking at the cost of each example.So, it tries to fit each training example a little bit better individually.
4. Mostly taking 1-10 passes through your entire dataset should give good results for stochastic gradient descent. 
5. When the training set is large, stochastic gradient is much faster.
6. The cost function does not necessarily go down with every pass for stochastic gradient descent.
   
Batch Gradient Descent:- Uses all m examples in each iteration<br>
Stochastic Gradient Descent- Uses 1 example in each iteration<br>
Mini Batch Gradient Descent - Uses b examples in each iteration (b is called the mini batch size 2-100)<br>
<br>
Stochastic gradient descent does not converge to the global minimum, it oscillates around the global minimum. A smaller learning rate in Stochastic Gradient descent may end up in a slightly better solution than one with a higher learning rate.<br>
It's possible that we obtain a smoother curve by averaging over, say 5,000 examples instead of 1,000. That's the effect of increasing the number of examples you average over. The disadvantage of making this too big  is that now you get one date point only every 5,000 examples. And so the feedback you get on how well your learning learning algorithm is doing,it's more delayed because you get one data point on your plot only every 5,000 examples rather than every 1000 examples. <br>

*When the average cost increases, it means the algorithm is diverging. Use a smaller learning rate alpha.*<br>

## Online Learning:

The problem of learning in online learning is actually called the problem of learning the predicted click-through rate, the predicted CTR. It just means learning the probability that the user will click on the specific link that you offer them, so CTR is an abbreviation for click through rate. Each time a user clicks on one of the ten recommended phones, we get 10 new training examples to train our algorithm.<br>

1. It can adapt to changing user tastes.
2. It learns from a continuous stream of data, as each example is only used once and is no longer processed again.
   
## Map Reduce:
Whenever your learning algorithm can be expressed as a sum of the training set and whenever the bulk of the work of the learning algorithm can be expressed as the sum of the training set, then map reviews might a good candidate for scaling your learning algorithms through good data sets.
