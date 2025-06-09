# Multi Class

A **multi-class model** is a type of machine learning model used when your task involves **classifying inputs into one of three or more possible categories**.


## How It Works

1. **Input Layer**

   * Receives raw input (e.g., image pixels, text tokens, tabular features)

2. **Hidden Layers**

   * Extract patterns using weights, activations, etc. (e.g., via neural networks)

3. **Output Layer**

   * Has **one neuron per class**
   * Outputs **raw scores (logits)** → passed to **softmax** to get probabilities

### Output Example (Logits → Probabilities):

```python
logits = [2.5, 1.0, 0.2]
softmax = [0.71, 0.21, 0.08]  # After softmax
```

Predicted class = class with highest probability → `0` in this case


## Training a Multi-Class Model

### Loss Function:

Use **Categorical Cross-Entropy** (a.k.a. Softmax Loss):

```math
L = -log(P[class_correct])
```

### Labels:

* One-hot encoded vector if using raw softmax:

```text
True label "Dog" → [0, 1, 0]
```

* Or use class indices with built-in loss functions like `CrossEntropyLoss` (PyTorch) or `SparseCategoricalCrossentropy` (TensorFlow)

## Common Model Architectures

| Type                  | Example Use Case                             |
| --------------------- | -------------------------------------------- |
| Fully connected (MLP) | Tabular data                                 |
| CNN                   | Image classification (e.g., MNIST, CIFAR-10) |
| RNN/LSTM/Transformer  | Text classification                          |

## Summary

| Component          | Details                              |
| ------------------ | ------------------------------------ |
| Output classes     | 3 or more (e.g., 10 for digits)      |
| Output layer       | Softmax to get probabilities         |
| Loss function      | Cross-entropy                        |
| Prediction         | `argmax(probabilities)`              |
| Evaluation metrics | Accuracy, Confusion Matrix, F1-score |