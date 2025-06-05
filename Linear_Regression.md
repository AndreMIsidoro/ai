# Linear Regression Model

A linear regression model is a type of supervised machine learning algorithm used to predict a continuous output (dependent variable) based on one or more input features (independent variables). It assumes a linear relationship between the input variables and the output.



## Multiple Linear Regression

Multiple Linear Regression models the relationship between one dependent variable and two or more independent variables.


### Euqations

    ŷ = w₁x₁ + w₂x₂ + ... + wₙxₙ + b

Vector Form:

    ŷ = wᵀx + b

Where:
- `ŷ` = predicted value
- `x = [x₁, x₂, ..., xₙ]` = input features
- `w = [w₁, w₂, ..., wₙ]` = weights
- `b` = bias (intercept term)

Cost Function - Mean Squared Error

    J(w, b) = (1 / 2m) * Σ (ŷ⁽ⁱ⁾ - y⁽ⁱ⁾)²

Where:
- `m` = number of training examples
- `ŷ⁽ⁱ⁾` = predicted value for i-th sample
- `y⁽ⁱ⁾` = actual value for i-th sample

Gradient Descent

    wⱼ := wⱼ - α * (1/m) * Σ (ŷ⁽ⁱ⁾ - y⁽ⁱ⁾) * xⱼ⁽ⁱ⁾
    b := b - α * (1/m) * Σ (ŷ⁽ⁱ⁾ - y⁽ⁱ⁾)

Where:
- `α` = learning rate
