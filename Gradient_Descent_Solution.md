# Gradient Descent Manual Calculation Solution

## Problem Setup

**Given:**
- Linear equation: $y = mx + b$
- Initial $m = -1$
- Initial $b = 1$
- Learning rate $\alpha = 0.1$
- Data points: $(1, 3)$ and $(3, 6)$

**Goal:** Perform 3 iterations of gradient descent to update $m$ and $b$

---

## Step 1: Derive the Gradient Formulas

**Cost Function (Mean Squared Error):**

$$J(m, b) = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2$$

where $\hat{y}_i = mx_i + b$ (predicted value)

**Partial Derivatives:**

For $m$:

$$\frac{\partial J}{\partial m} = \frac{1}{n} \sum_{i=1}^{n} 2(y_i - \hat{y}_i) \cdot (-x_i) = -\frac{2}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i) \cdot x_i$$

For $b$:

$$\frac{\partial J}{\partial b} = \frac{1}{n} \sum_{i=1}^{n} 2(y_i - \hat{y}_i) \cdot (-1) = -\frac{2}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)$$

**Update Rules:**

$$m_{new} = m_{old} - \alpha \cdot \frac{\partial J}{\partial m}$$

$$b_{new} = b_{old} - \alpha \cdot \frac{\partial J}{\partial b}$$

---

## ITERATION 0 (Initial Values)

**Parameters:**
- $m_0 = -1$
- $b_0 = 1$

---

## ITERATION 1

### Step 1: Calculate Predictions ($\hat{y}$)

For point $(1, 3)$:
$$\hat{y}_1 = m \cdot x_1 + b = (-1) \cdot 1 + 1 = -1 + 1 = 0$$

For point $(3, 6)$:
$$\hat{y}_2 = m \cdot x_2 + b = (-1) \cdot 3 + 1 = -3 + 1 = -2$$

### Step 2: Calculate Errors

For point $(1, 3)$:
$$\text{error}_1 = y_1 - \hat{y}_1 = 3 - 0 = 3$$

For point $(3, 6)$:
$$\text{error}_2 = y_2 - \hat{y}_2 = 6 - (-2) = 8$$

### Step 3: Calculate Gradients

**Gradient for $m$:**
$$\frac{\partial J}{\partial m} = -\frac{2}{2} [(3) \cdot 1 + (8) \cdot 3]$$
$$= -1 [3 + 24]$$
$$= -1 \cdot 27 = -27$$

**Gradient for $b$:**
$$\frac{\partial J}{\partial b} = -\frac{2}{2} [(3) + (8)]$$
$$= -1 \cdot 11 = -11$$

### Step 4: Update Parameters

**Update $m$:**
$$m_1 = m_0 - \alpha \cdot \frac{\partial J}{\partial m}$$
$$m_1 = -1 - (0.1) \cdot (-27)$$
$$m_1 = -1 + 2.7 = 1.7$$

**Update $b$:**
$$b_1 = b_0 - \alpha \cdot \frac{\partial J}{\partial b}$$
$$b_1 = 1 - (0.1) \cdot (-11)$$
$$b_1 = 1 + 1.1 = 2.1$$

**New Parameters:** $m_1 = 1.7$, $b_1 = 2.1$

---

## ITERATION 2

### Step 1: Calculate Predictions ($\hat{y}$)

For point $(1, 3)$:
$$\hat{y}_1 = 1.7 \cdot 1 + 2.1 = 1.7 + 2.1 = 3.8$$

For point $(3, 6)$:
$$\hat{y}_2 = 1.7 \cdot 3 + 2.1 = 5.1 + 2.1 = 7.2$$

### Step 2: Calculate Errors

For point $(1, 3)$:
$$\text{error}_1 = 3 - 3.8 = -0.8$$

For point $(3, 6)$:
$$\text{error}_2 = 6 - 7.2 = -1.2$$

### Step 3: Calculate Gradients

**Gradient for $m$:**
$$\frac{\partial J}{\partial m} = -\frac{2}{2} [(-0.8) \cdot 1 + (-1.2) \cdot 3]$$
$$= -1 [-0.8 + (-3.6)]$$
$$= -1 \cdot (-4.4) = 4.4$$

**Gradient for $b$:**
$$\frac{\partial J}{\partial b} = -\frac{2}{2} [(-0.8) + (-1.2)]$$
$$= -1 \cdot (-2.0) = 2.0$$

### Step 4: Update Parameters

**Update $m$:**
$$m_2 = m_1 - \alpha \cdot \frac{\partial J}{\partial m}$$
$$m_2 = 1.7 - (0.1) \cdot (4.4)$$
$$m_2 = 1.7 - 0.44 = 1.26$$

**Update $b$:**
$$b_2 = b_1 - \alpha \cdot \frac{\partial J}{\partial b}$$
$$b_2 = 2.1 - (0.1) \cdot (2.0)$$
$$b_2 = 2.1 - 0.2 = 1.9$$

**New Parameters:** $m_2 = 1.26$, $b_2 = 1.9$

---

## ITERATION 3

### Step 1: Calculate Predictions ($\hat{y}$)

For point $(1, 3)$:
$$\hat{y}_1 = 1.26 \cdot 1 + 1.9 = 1.26 + 1.9 = 3.16$$

For point $(3, 6)$:
$$\hat{y}_2 = 1.26 \cdot 3 + 1.9 = 3.78 + 1.9 = 5.68$$

### Step 2: Calculate Errors

For point $(1, 3)$:
$$\text{error}_1 = 3 - 3.16 = -0.16$$

For point $(3, 6)$:
$$\text{error}_2 = 6 - 5.68 = 0.32$$

### Step 3: Calculate Gradients

**Gradient for $m$:**
$$\frac{\partial J}{\partial m} = -\frac{2}{2} [(-0.16) \cdot 1 + (0.32) \cdot 3]$$
$$= -1 [-0.16 + 0.96]$$
$$= -1 \cdot 0.8 = -0.8$$

**Gradient for $b$:**
$$\frac{\partial J}{\partial b} = -\frac{2}{2} [(-0.16) + (0.32)]$$
$$= -1 \cdot 0.16 = -0.16$$

### Step 4: Update Parameters

**Update $m$:**
$$m_3 = m_2 - \alpha \cdot \frac{\partial J}{\partial m}$$
$$m_3 = 1.26 - (0.1) \cdot (-0.8)$$
$$m_3 = 1.26 + 0.08 = 1.34$$

**Update $b$:**
$$b_3 = b_2 - \alpha \cdot \frac{\partial J}{\partial b}$$
$$b_3 = 1.9 - (0.1) \cdot (-0.16)$$
$$b_3 = 1.9 + 0.016 = 1.916$$

**New Parameters:** $m_3 = 1.34$, $b_3 = 1.916$

---

## Summary Table

| Iteration | $m$ | $b$ | Error Point 1 | Error Point 2 | $\frac{\partial J}{\partial m}$ | $\frac{\partial J}{\partial b}$ |
|-----------|-----|-----|---------------|---------------|---------------------------------|---------------------------------|
| 0 | -1 | 1 | - | - | - | - |
| 1 | 1.7 | 2.1 | 3 | 8 | -27 | -11 |
| 2 | 1.26 | 1.9 | -0.8 | -1.2 | 4.4 | 2.0 |
| 3 | 1.34 | 1.916 | -0.16 | 0.32 | -0.8 | -0.16 |

---

## Trend Observation

**Are $m$ and $b$ moving towards reducing the error?**

**YES!** Here's why:

1. **Error magnitude is decreasing:**
   - Iteration 1: Large errors (3, 8) - predictions were way off
   - Iteration 2: Smaller errors (-0.8, -1.2) - much closer to actual values
   - Iteration 3: Even smaller errors (-0.16, 0.32) - very close to actual values

2. **Parameters are converging:**
   - $m$ changed dramatically from -1 → 1.7, then gradually: 1.7 → 1.26 → 1.34
   - $b$ changed from 1 → 2.1, then gradually: 2.1 → 1.9 → 1.916
   - The changes are getting smaller, indicating convergence

3. **The line is fitting better:**
   - Initial line: $y = -1x + 1$ (completely wrong direction)
   - After 3 iterations: $y = 1.34x + 1.916$ (much better fit)
   - The actual best fit for points (1,3) and (3,6) is approximately $y = 1.5x + 1.5$

**Conclusion:** The gradient descent algorithm is successfully minimizing the error and finding parameters that better fit the data points!

---

## Key Takeaways

1. **Gradient descent iteratively improves parameters** by moving in the direction opposite to the gradient
2. **The learning rate ($\alpha = 0.1$)** controls how big each step is
3. **Errors get smaller** with each iteration, showing the algorithm is working
4. **The gradient tells us which direction and how much to adjust** each parameter
5. **Eventually, the parameters converge** to values that minimize the cost function
