Regression is used to predict a number

**Linear Regression**
A linear relationship - that is a straight line trough a graph, can be represented as:
$y = mx +b$ 

In ML we write this in the following way. 
$y' = b +w^1x^1$ 

where:
- y = variable we want to predict / Predicted Label
- m = slope of line / w = Weight of the feature
- x = value of our input / Feature
- b = y intercept.

Weights are chosen to minimise the sum of the squares of the errors.

Squaring the error is done for the following reason:

- Always produces a positive number, wether error is positive or negative.
- Amplifies large errors compared to small ones.

Least absolute deviation can also be used for linear regression, and this minimises the sum of the absolute values of errors.

## Logistic regression
Efficient method for calculating probabilities.

This is done by taking the result of a linear function and passing it through a logistic function.

We can map the output into the solution to a binary classification problem.

Sigmoid function makes sure that output is always between 0 and 1

$y = 1/(1 + e^z)$ 

The loss function for linear regression is squared loss. Log loss.

$z = log(\cfrac{y}{1-y})$ 

Regularisation is very important in logistic regression modelling.