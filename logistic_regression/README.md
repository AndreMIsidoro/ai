# Logistic Regression

**Logistic Regression** is a statistical model used for **binary classification**. It estimates the **probability** that a given input belongs to a particular class.

## Model

### 1. Linear Combination

We compute a **weighted sum** of the input features:

```math
z = w_1x_1 + w_2x_2 + \cdots + w_nx_n + b = \mathbf{w}^\top \mathbf{x} + b
```

### 2. Sigmoid Activation

To convert `z` to a **probability**, we use the **sigmoid function**:

```math
\sigma(z) = \frac{1}{1 + e^{-z}}
```

This maps any real number to the range (0, 1).

### 3. Prediction

The output is interpreted as:

```math
\hat{y} = \sigma(\mathbf{w}^\top \mathbf{x} + b)
```

We classify based on a threshold (typically 0.5):

```math
\hat{y} = 
\begin{cases}
1 & \text{if } \sigma(z) \geq 0.5 \\
0 & \text{if } \sigma(z) < 0.5
\end{cases}
```

## Loss Function: Binary Cross-Entropy

To train the model, we minimize the **binary cross-entropy loss**:

```math
\mathcal{L}(y, \hat{y}) = - \left[ y \log(\hat{y}) + (1 - y) \log(1 - \hat{y}) \right]
```

Where:

* $y$ is the true label
* $\hat{y}$ is the predicted probability


## Training: Gradient Descent

We update the weights via **gradient descent**:

```math
w := w - \alpha \frac{\partial \mathcal{L}}{\partial w}
```

```math
b := b - \alpha \frac{\partial \mathcal{L}}{\partial b}
```

Where $\alpha$ is the **learning rate**.


## Use Case

Logistic Regression is ideal when:

* The output is binary (0 or 1)
* You want interpretable coefficients
* The relationship between input and log-odds is linear


## Summary

| Feature       | Description                    |
| ------------- | ------------------------------ |
| Type          | Classification                 |
| Output        | Probability (0–1)              |
| Activation    | Sigmoid                        |
| Loss Function | Binary Cross-Entropy           |
| Optimization  | Gradient Descent (or variants) |
