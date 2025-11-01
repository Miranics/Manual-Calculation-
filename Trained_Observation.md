# Trend Observation — Gradient Descent (Concise)

- Error magnitudes decreased across iterations:
  - Iteration 1 errors: 3 and 8
  - Iteration 2 errors: 0.8 and 1.2 (absolute values)
  - Iteration 3 errors: 0.16 and 0.32 (absolute values)

- Parameters moved toward a stable solution:
  - m: -1 → 1.7 → 1.26 → 1.34 (large initial jump, then smaller adjustments)
  - b: 1 → 2.1 → 1.9 → 1.916 (converging)

- Updates decreased in size over iterations, indicating convergence toward the minimum of the mean squared error.

Conclusion: Gradient descent successfully reduced prediction error for these two points and adjusted the slope and intercept toward values that better fit the data. The learning rate determined step sizes; as the model approached the minimum, parameter changes became smaller.
