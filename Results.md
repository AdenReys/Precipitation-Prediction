# Model Results - kNN and Weighted kNN (Normalized vs Non-normalized)

## Summary of Results

### kNN (3 Neighbors)
- **R²**: -0.1071
- **MAE**: 0.267
- **MSE**: 0.294

### Best kNN Model (after fine-tuning with 10 neighbors)
- **R²**: 0.1653
- **MAE**: 0.218
- **MSE**: 0.222

### kNN (Normalized Data)
- **R²**: 0.0385
- **MAE**: 0.224
- **MSE**: 0.255

### Non-normalized Weighted kNN
- **Predicted Value**: 0.22
- **MAE**: 0.30
- **R²**: 0.00
- **MSE**: 0.18

### Normalized Weighted kNN
- **Predicted Value**: 0.22
- **MAE**: 0.30
- **R²**: 0.00
- **MSE**: 0.18

## Key Observations:
1. **kNN Models**: The kNN models (both with 3 neighbors and the best model with 10 neighbors) showed **negative or very low R² values**, indicating that the model struggled to capture the variance of the target variable. This was especially evident in the 3-neighbor kNN model, which resulted in a negative R² score.
2. **Normalized kNN**: The normalized kNN model yielded slightly better performance than the non-normalized kNN in terms of **MAE** and **MSE**, but the **R²** value remains low, suggesting a poor fit.
3. **Weighted kNN**: Both the non-normalized and normalized weighted kNN models produced identical results for **MAE**, **MSE**, and **R²**. This suggests that the weighting did not have a significant impact in this specific test case.

## Visualizing Model Performance

To visualize the comparison between the models, the following metrics were considered: **R² Score**, **Mean Absolute Error (MAE)**, and **Mean Squared Error (MSE)**.

### Bar Plot Representation of the Results:

```python
import matplotlib.pyplot as plt

# Define model names and corresponding metric values
models = ['kNN (3 Neighbors)', 'Best kNN (10 Neighbors)', 'kNN (Normalized)', 'Weighted kNN (Non-Normalized)', 'Weighted kNN (Normalized)']
r2_values = [-0.1071, 0.1653, 0.0385, 0.00, 0.00]
mae_values = [0.267, 0.218, 0.224, 0.30, 0.30]
mse_values = [0.294, 0.222, 0.255, 0.18, 0.18]

# Create bar plots for each metric
plt.figure(figsize=(15, 6))

# R² Plot
plt.subplot(1, 3, 1)
plt.bar(models, r2_values, color='blue')
plt.title('R² Score')
plt.ylabel('R²')
plt.ylim(-0.2, 0.4)

# MAE Plot
plt.subplot(1, 3, 2)
plt.bar(models, mae_values, color='green')
plt.title('Mean Absolute Error (MAE)')
plt.ylabel('MAE')

# MSE Plot
plt.subplot(1, 3, 3)
plt.bar(models, mse_values, color='red')
plt.title('Mean Squared Error (MSE)')
plt.ylabel('MSE')

plt.tight_layout()
plt.show()
