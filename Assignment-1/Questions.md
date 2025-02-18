# Linear Regression

1. What are the pros and cons of using the normal equation to solve for the weights in linear regression as opposed to using gradient descent?

 There are several pros and cons to using the normal equation to solve for the weights in linear regression as opposed to using gradient descent:

# Pros of the normal equation:
- It is guaranteed to converge to the optimal solution in a single step, whereas gradient descent may require multiple iterations.
- It is computationally efficient, especially for small datasets.
- Unlike gradient descent, it doesn’t require choosing a learning rate or iterating over multiple epochs
# Cons of the normal equation:
- It requires the inverse of the Hessian matrix, which can be computationally expensive for large datasets
- It can be numerically unstable if the Hessian matrix is ill-conditioned.
- Memory constraints: Requires storing the full 𝑋 𝑇 𝑋 matrix in memory, which is infeasible for very large datasets.
# Pros of gradient descent:
- It is computationally efficient for large datasets.
- It can be used for non-linear regression and other machine learning algorithms.
- Can be applied to non-invertible X T X: If X T X is singular, gradient descent still works, whereas the normal equation would fail.
# Cons of gradient descent:
- It may not converge to the optimal solution, especially if the learning rate is too high or too low.
- It can be computationally expensive for large datasets.

# Logistic Regression
1. Why is the softmax function used in multi-class logistic regression (Hint: the model itself produces logits)?

The softmax function is used in multi-class logistic regression because it maps the logits (the output of the model) to a probability distribution over the classes. The logits are not probabilities, but rather a vector of real numbers that represent the relative likelihood of each class. The softmax function takes the logits and normalizes them to produce a probability distribution over the classes. This is necessary because the model produces logits, not probabilities, and we need to produce a probability distribution over the classes to make predictions. The softmax function is defined as:   softmax(x) = exp(x) / Σ exp(x), where x is the vector of logits. This function is used to ensure that the output of the model is a valid probability distribution, where the probability of each class is between 0 and 1, and the sum of the probabilities over all classes is 1. 