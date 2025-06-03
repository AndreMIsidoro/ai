# Cost Function

The **cost function** measures how well the model's predictions match the actual data. It quantifies the **error** between predicted values (`ŷ`) and true values (`y`).


## Mean Squared Error (MSE)

J(θ) = (1 / 2m) * Σ from i=1 to m of (ŷ⁽ⁱ⁾ - y⁽ⁱ⁾)²

Where:
- J(θ) = cost function
- m = number of training examples
- ŷ⁽ⁱ⁾ = predicted value for the i-th example
- y⁽ⁱ⁾ = actual value for the i-th example
- θ = model parameters

---
- Penalizes large errors more
- Always positive
- Smooth and differentiable