# Gradient Descent

Gradient Descent is an optimization algorithm used to minimize a cost (or loss) function (finds the local minimum) by iteratively updating model parameters in the opposite direction of the gradient.


## Update Rule

For each parameter θ:

    θ := θ - α * ∂J(θ)/∂θ

Where:
- `θ` is a model parameter (like `w` or `b`)
- `α` is the learning rate (step size)
- `∂J(θ)/∂θ` is the partial derivative of the cost function with respect to θ


## Example For Linear Regression

Given:

    y_hat = w * x + b

Cost Function:

    J(w, b) = (1 / 2m) * Σ (y_hat_i - y_i)^2

Gradient Descent update steps:

    w := w - α * (1/m) * Σ (y_hat_i - y_i) * x_i  
    b := b - α * (1/m) * Σ (y_hat_i - y_i)

Repeat these updates for several iterations until convergence.


## Notes

- Too high `α` → Divergence (overshoots minimum)
- Too low `α` → Slow convergence
- Can be improved with techniques like:
  - Learning rate schedules
  - Momentum
  - Adam optimizer (for deep learning)