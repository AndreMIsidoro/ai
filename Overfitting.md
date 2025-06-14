# Overfitting

**Overfitting** happens when your machine learning model learns **not only the true patterns** in the training data but also the **noise and random fluctuations**.

As a result:

* It performs *very well* on training data
* But *poorly* on new, unseen data (bad generalization)


## Symptoms of Overfitting

| Metric             | Training Set                       | Validation/Test Set      |
| ------------------ | ---------------------------------- | ------------------------ |
| Accuracy / Loss    | High Accuracy / Low Loss           | Low Accuracy / High Loss |
| Gap Between Scores | Small loss on train, large on test | ➜ RED FLAG 🚩            |

##  Common Causes

* Model is **too complex** (e.g., too many layers or features)
* **Too little training data**
* **Too many training epochs**
* No regularization (e.g., no dropout or weight decay)

## Fixes for Overfitting

| Method                | Description                               |
| --------------------- | ----------------------------------------- |
| **More Data**         | Helps the model learn general patterns    |
| **Regularization**    | Penalizes complexity (e.g., L1/L2)        |
| **Dropout**           | Randomly disables neurons during training |
| **Early Stopping**    | Stop training before the model overfits   |
| **Cross-Validation**  | Ensures model generalizes across folds    |
| **Simplify Model**    | Reduce parameters/layers/features         |
| **Data Augmentation** | Increase data variability artificially    |

## Rule of Thumb

If your model performs **great on training** but **bad on test**, it’s likely **overfitting**.