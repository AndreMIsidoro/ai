# Softmax

The **softmax function** is commonly used in **multi-class classification** to convert a vector of raw scores (logits) into a vector of **probabilities**.

## Formula

Given a vector of logits `z = [z₁, z₂, ..., zₙ]`, the softmax function is defined as:

```math
softmax(zᵢ) = exp(zᵢ) / Σⱼ exp(zⱼ)
```

Where:

* `exp(zᵢ)` is the exponential of the `i-th` logit
* The denominator is the sum of exponentials of all logits

## Use in Neural Networks

* Applied at the **final layer** of a classifier
* Often used with **cross-entropy loss**
* Helps convert raw output scores into interpretable probabilities


## Intuition

Softmax:

* Exaggerates the **highest score**
* Suppresses **lower scores**
* Ensures **probabilities sum to 1**

## Summary

| Component   | Description                                   |
| ----------- | --------------------------------------------- |
| Input       | Vector of logits (real numbers)               |
| Output      | Vector of probabilities (sums to 1)           |
| Typical use | Final layer in multi-class classifiers        |
| Properties  | Differentiable, smooth, amplifies differences |