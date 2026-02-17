# credit-card-sampling-analysis
# 💳 Credit Card Fraud Detection  
### Sampling Techniques Comparison on Imbalanced Dataset

---

## 📌 Project Overview

This project investigates how different **sampling strategies** impact machine learning performance on an **imbalanced credit card fraud dataset** (`Creditcard_data.csv`).

The target column `Class` represents:

- `0` → Normal transaction  
- `1` → Fraudulent transaction  

Since fraud cases are very rare, traditional ML models become biased toward non-fraud samples. To solve this, multiple resampling techniques were applied and evaluated.

---

## 🎯 Objective

To compare various **under-sampling and over-sampling methods** and identify which combination of model + sampling gives the best accuracy.

---

## ⚙️ Machine Learning Models

Five models were trained on each resampled dataset:

- Logistic Regression  
- Decision Tree  
- Random Forest  
- Support Vector Machine (SVM)  
- XGBoost  

---

## 🧪 Sampling Techniques Used

- Random Under Sampling (manual)
- Random Over Sampling (manual)
- Random Under Sampling (imblearn)
- Random Over Sampling (imblearn)
- SMOTE

---

## 📊 Accuracy Results (Sample)

| Model | RUS | ROS | RUS (imblearn) | ROS (imblearn) | SMOTE |
|------|-----|-----|---------------|---------------|-------|
| Logistic Regression | 25.00 | 93.46 | 25.00 | 93.46 | 90.85 |
| Decision Tree | 75.00 | 99.35 | 75.00 | 99.35 | 97.71 |
| Random Forest | 25.00 | 100.00 | 25.00 | 100.00 | 99.35 |
| SVM | 0.00 | 66.99 | 0.00 | 66.99 | 68.63 |
| XGBoost | 75.00 | 99.67 | 75.00 | 99.67 | 99.02 |

Full results are stored in:
results_matrix.csv


---

## 🏆 Best Sampling Technique per Model

- Logistic Regression → Random Over Sampling (93.46%)
- Decision Tree → Random Over Sampling (99.35%)
- Random Forest → Random Over Sampling (100%)
- SVM → SMOTE (68.63%)
- XGBoost → Random Over Sampling (99.67%)

---

## 📈 Visualizations

Generated plots are available :
heatmap.png

accuracy_bar_chart.png


- Heatmap: Model vs Sampling Accuracy
- <img width="2771" height="1638" alt="image" src="https://github.com/user-attachments/assets/e0b2945a-a8d9-4a05-bc83-15d9f16b63cb" />

- Bar Chart: Overall Accuracy Comparison
<img width="3820" height="2066" alt="image" src="https://github.com/user-attachments/assets/8299d43e-8550-4201-8a49-376f17d226a7" />

---

## 🚀 Key Insights

- Random Over Sampling consistently provided the best performance for most models.
- SMOTE improved SVM results compared to basic sampling.
- Tree-based models (Decision Tree, Random Forest, XGBoost) achieved near-perfect accuracy after oversampling.
- Simple under-sampling caused information loss and reduced performance.

---

## 🧠 Conclusion

Proper handling of class imbalance is critical in fraud detection.

This project shows that **sampling strategy often matters more than model choice** when working with skewed datasets.

---





