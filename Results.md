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

![Uploading Untitled.png…]()

#### **kNN vs. Normalized kNN**
✅ The **normalized kNN (k=3)** performed better than the non-normalized kNN across all metrics (**R², MAE, MSE**), indicating that normalizing the data improved the model's performance.  
✅ After fine-tuning, the **best kNN model** had **10 neighbors**, leading to further improvements in **R², MAE, and MSE**, proving that adjusting the number of neighbors enhances accuracy.  

#### **Weighted kNN vs. Normalized Weighted kNN**  
✅ Both **weighted kNN** and **normalized weighted kNN** performed similarly.  
✅ **R² was close to 0, and MSE was relatively low**, meaning the predictions were off by a consistent margin.  
✅ The weighted kNN approach did **not significantly improve** the model.  

#### **Decision Tree vs. Fine-Tuned Decision Tree**  
🚫 The initial **Decision Tree** model performed poorly (**negative R², high MSE & MAE**), likely due to **overfitting or poor generalization**.  
✅ **Fine-tuning the Decision Tree** (by adjusting **max depth to 2**) significantly improved performance, leading to **positive R²** and lower errors.  

#### **Challenges (Bumps in the Road)**  
❌ **Could not normalize Decision Tree data**  
❌ **Could not normalize Random Forest data**  
