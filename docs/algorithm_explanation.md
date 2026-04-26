# Naive Bayes Algorithm - Detailed Explanation

## What is Naive Bayes?

Naive Bayes is a **probabilistic machine learning algorithm** used for classification tasks. It is based on **Bayes' Theorem** and assumes that all features are independent of each other — hence the term "Naive".

## Bayes' Theorem

The core of the Naive Bayes algorithm is Bayes' Theorem:

```
P(Ck|X) = P(X|Ck) * P(Ck) / P(X)
```

Where:
- **P(Ck|X)** = Posterior probability (probability of class Ck given features X)
- **P(X|Ck)** = Likelihood (probability of features X given class Ck)
- **P(Ck)** = Prior probability (probability of class Ck)
- **P(X)** = Evidence (probability of features X)

## Why "Naive"?

The algorithm makes a **naive assumption** that all features are conditionally independent given the class label. This means:

```
P(X|Ck) = P(x1|Ck) * P(x2|Ck) * ... * P(xn|Ck)
```

In reality, features often have dependencies, but the algorithm still performs well in practice.

## Gaussian Naive Bayes (GaussianNB)

GaussianNB is a variant of Naive Bayes that assumes the features follow a **Gaussian (Normal) distribution**. This is ideal for continuous numerical data.

### How It Works

1. **Estimate Parameters**: For each class, calculate the mean and variance of each feature from the training data.
2. **Calculate Likelihood**: Use the Gaussian probability density function to compute the likelihood of each feature.
3. **Apply Bayes' Theorem**: Combine likelihoods with prior probabilities to get the posterior.
4. **Predict**: Assign the class with the highest posterior probability.

### Gaussian Probability Density Function

```
P(xi|Ck) = (1 / sqrt(2*pi*sigma^2)) * exp(-(xi - mu)^2 / (2*sigma^2))
```

Where:
- **mu** = mean of feature xi for class Ck
- **sigma** = standard deviation of feature xi for class Ck

## Advantages

- Fast and efficient, even on small datasets
- Works well with high-dimensional data
- Simple to implement and interpret
- Requires less training data
- Performs well even when independence assumption is violated

## Disadvantages

- Assumes feature independence (rarely true in real-world data)
- Cannot handle zero-frequency problem without smoothing
- Performance can degrade with highly correlated features

## When to Use GaussianNB

- Small to medium-sized datasets
- Text classification (spam detection, sentiment analysis)
- Medical diagnosis
- Real-time prediction systems
- As a baseline model for classification tasks

## References

1. Fisher, R.A. (1936). "The use of multiple measurements in taxonomic problems". *Annals of Eugenics*.
2. Scikit-learn documentation: https://scikit-learn.org/stable/modules/naive_bayes.html
3. Bishop, C.M. (2006). *Pattern Recognition and Machine Learning*. Springer.

---
*This document is part of the Naive Bayes Algorithm - GaussianNB project.*
