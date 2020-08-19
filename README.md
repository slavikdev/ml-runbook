# ML Runbook

Collection of solutions for common ML problems. Contributions welcome :)

## Dataset

### When to use large dataset

- If you have high variance (overfitting).
- If the features are good enough for prediciton and a human expert can do manual estimation based on them.
- If the algorithm has many parameters and can represent fairly complex functions.

## High Variance (overfitting)

Your model is performing very well on the training set, but poorly on the test set.

### In general

- Try getting more training examples.
- Try smaller set of features.
- When using regularization, try increasing the `lambda` parameter.

### SVM

- Try decreasing the parameter `C` (1/lambda).
- Try increasing the parameter `sigma^2`.

## High Bias (underfitting)

Your model performs poorly on both training and test sets.

### In general

- Try adding more features features
- Try adding polynomial features i.e. `x^2`, `x1*x2` etc.
- When using regularization, try decreasing the `lambda` parameter.

### SVM

- Try increasing the parameter `C` (1/lambda).
- Try decreasing the parameter `sigma^2`.

## Choosing the right classifier

### Logistic regression vs SVM

- If the number of features is large (relative to the number of examples), use either logistic regression or SVM without a kernel.
- If the number of features is small and the number of examples is intermediate (up to 10K), use SVM with Gaussian kernel.
- If the number of features is small, but the number of examples is large (over 10k), create/add more features, then use logistic regression or SVM without a kernel.
