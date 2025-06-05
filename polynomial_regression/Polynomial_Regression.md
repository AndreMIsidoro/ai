# Polynomial Regression

**Polynomial Regression** is a type of regression that models the relationship between a dependent variable `y` and one or more independent variables `x` as an n-th degree polynomial.

It extends linear regression by allowing for **non-linear relationships**.

## Equation

For a single variable:

    y = w₀ + w₁x + w₂x² + w₃x³ + ... + wₙxⁿ

Where

- `y`: predicted value  
- `x`: input feature  
- `w₀`: intercept (bias)  
- `w₁, ..., wₙ`: weights/coefficients  
- `n`: degree of the polynomial

## Why Use It?

Polynomial regression can capture:
- Non-linear trends
- Curved patterns in data
- More accurate fits for complex datasets

It is **still a linear model** in terms of coefficients (despite the non-linear input terms), which means it's solvable using linear regression techniques.

##  Caveats

- Too high a degree → **Overfitting**
- Too low a degree → **Underfitting**
- Use **cross-validation** to choose the optimal degree

## When to Use It

| Use Case                          | Recommended Polynomial Degree |
|-----------------------------------|-------------------------------|
| Slight curve in data              | 2 or 3                        |
| Moderate non-linear relationship  | 3 to 4                        |
| Highly complex patterns           | 5 or higher                   |
| Small dataset (risk of overfitting)| 2 or lower                    |
| Want model interpretability       | 2 or lower                    |
