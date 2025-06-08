#Feature Scaling

Feature scaling is a preprocessing technique used to normalize the range of independent variables (features) in your dataset. It's essential for machine learning algorithms that are sensitive to the scale of the data.

## Why Use Feature Scaling?

Some ML models rely heavily on feature magnitude:

- **Sensitive to feature scale**:
  - Linear Regression (with Gradient Descent)
  - Logistic Regression
  - SVM
  - KNN
  - Neural Networks
  - K-Means Clustering

- **Not sensitive to scale**:
  - Decision Trees
  - Random Forest
  - Gradient Boosted Trees (like XGBoost)

## Common Methods

### Min-Max Scaling

Scales the data to a fixed range, usually [0, 1].

Formula:

    x' = (x - min(x)) / (max(x) - min(x))


- Maintains shape of distribution
- Sensitive to outliers

### Standardization (Z-Score Normalization)

Centers features around 0 with standard deviation 1.

Formula:

    x' = (x - mean(x)) / std(x)


- Works well with outliers
- Ideal for models assuming normally distributed data

### Robust Scaling

Uses median and interquartile range to reduce the influence of outliers.

Formula:

    x' = (x - median(x)) / IQR(x)

- Most robust to outliers

| Method            | Outlier Tolerance | Output Range | Best For                            |
|-------------------|-------------------|--------------|--------------------------------------|
| Min-Max Scaling   |  No              | [0, 1]       | Normalizing bounded data            |
| Standardization   |  Yes             | ~[-3, 3]     | Gradient-based models (e.g., SVM)   |
| Robust Scaling    |  Very High     | Varies       | Data with many outliers             |
