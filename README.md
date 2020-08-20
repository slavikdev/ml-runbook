# ML Runbook

Collection of solutions for common ML problems. Contributions are welcome :)

## Dataset

### When to use a large dataset

- If you have high variance (overfitting).
- If the features are good enough for prediciton and a human expert can do manual estimation based on them.
- If the algorithm has many parameters and can represent fairly complex functions.

## High variance (overfitting)

Your model is performing very well on the training set, but poorly on the test set.

### In general

- Try getting more training examples.
- Try smaller set of features.
- When using regularization, try increasing the `lambda` parameter.

### SVM

- Try decreasing the parameter `C` (1/lambda).
- Try increasing the parameter `sigma^2`.

## High bias (underfitting)

Your model performs poorly on both training and test sets.

### In general

- Try adding more features features
- Try adding polynomial features i.e. `x^2`, `x1*x2` etc.
- When using regularization, try decreasing the `lambda` parameter.

### SVM

- Try increasing the parameter `C` (1/lambda).
- Try decreasing the parameter `sigma^2`.

## Choosing the right algorithm

### Logistic regression vs SVM

- If the number of features is large (relative to the number of examples), use either logistic regression or SVM without a kernel.
- If the number of features is small and the number of examples is intermediate (up to 10K), use SVM with Gaussian kernel.
- If the number of features is small, but the number of examples is large (over 10k), create/add more features, then use logistic regression or SVM without a kernel.

### Anomaly detection vs supervised learning

When to use anomaly detection algorithm (e.g. Gaussian distribution):

- You expect a very small number of anomalies (up to 20) and a large number of non-anomalous examples.
- You expect different types of anomalies and future anomalies may look like nothing you’ve seen so far.

When to use supervised learning:

- You expect a relatively large number of anomalies.
- Future examples are likely to be similar to the ones in the training set.
