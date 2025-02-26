# Random Forest Classifier

## Overview

The RandomForestClassifier is a machine learning model used for classification tasks. It is part of the ensemble learning family and works by combining multiple decision trees to make more accurate and robust predictions.

## How it Works

Creates multiple decision trees

- The model builds several Decision Trees on random subsets of the dataset (bagging method).

Each tree votes on the class

- Each tree predicts a class (0 or 1), and the final prediction is based on a majority vote.

Reduces overfitting

- Unlike a single Decision Tree, a Random Forest generalizes better, reducing overfitting.

## Key Features

- Handles both binary and multi-class classification
- Robust to noise and missing data
- Works well with high-dimensional data
- Less overfitting compared to Decision Trees
- Provides feature importance scores

## When To Use RandomForestClassifier

- When you need a robust classifier with minimal tuning
- When you have a mix of numerical and categorical features
- When overfitting is a concern
- For feature importance analysis

## Example


```python
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score, classification_report, confusion_matrix

model = RandomForestClassifier(n_estimators=100, random_state=42)
model.fit(X_train, y_train)
y_pred = model.predict(X_test)
print(f"Accuracy: {accuracy_score(y_test, y_pred):.4f}")
print(confusion_matrix(y_test, y_pred))
print(classification_report(y_test, y_pred))
```
