# 🚦 Crash Severity Prediction using Machine Learning

## 📌 Project Overview
This project focuses on predicting **crash severity (minor vs major)** using historical traffic crash data. By leveraging machine learning techniques, the goal is to uncover patterns in crash conditions and build a model that can support **data-driven road safety decisions**.

The project follows a structured workflow:
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Model Development (Baseline → Advanced)
- Model Evaluation & Comparison
- Business Interpretation

---

## 🎯 Objectives
- Predict whether a crash is **minor or major**
- Handle **class imbalance** effectively
- Compare multiple models and select the best performer
- Translate model results into **actionable insights**

---

## 📂 Project Structure
crash-severity-ml/

├── analysis.ipynb # Data exploration, visualization, feature engineering
├── modeling.ipynb # Model training, evaluation, predictions
├── README.md # Project documentation
└── data)


---

## 🧪 Approach

### 1. Exploratory Data Analysis
- Analyzed crash trends across **time, weather, and road conditions**
- Key observations:
  - Higher crash severity during **nighttime**
  - Influence of **weather conditions**
  - Impact of **number of vehicles involved**

---

### 2. Feature Engineering
To improve model performance, several features were engineered:

- **Interaction Features**
  - `hour × weather_severity`
- **Binned Features**
  - Temperature grouped into ranges
- **Derived Features**
  - Night vs Day
  - Rush hour indicators

These features helped capture **non-linear relationships** in the data.

---

### 3. Models Used

| Model | Purpose |
|------|--------|
| Logistic Regression | Baseline model |
| Random Forest | Capture non-linear patterns |
| Random Forest + SMOTE | Handle class imbalance |
| XGBoost | Final optimized model |

---

## 📊 Evaluation Metrics

Due to class imbalance, the primary evaluation metric used was:

- **Macro F1-score** → ensures balanced performance across both classes

Additional metrics:
- Accuracy
- Precision & Recall (per class)
- ROC Curve & AUC

---

## 📈 Results Summary

| Model | Accuracy | Class 0 Recall | Class 1 Recall | Macro F1 |
|------|----------|---------------|---------------|----------|
| Logistic Regression | 0.65 | 0.21 | 0.91 | 0.54 |
| Random Forest | 0.64 | 0.31 | 0.84 | 0.57 |
| RF + SMOTE | 0.62 | 0.49 | 0.69 | 0.59 |
| **XGBoost** | 0.62 | **0.65** | 0.60 | **0.61** |

✅ XGBoost achieved the **best balance across classes**

---

## 🔁 Cross-Validation

- 5-fold **Stratified Cross-Validation**
- Mean Macro F1: **0.61**
- Low variance → model is **stable and generalizable**

---

## 📉 Visualizations

- ROC Curve (multi-model comparison)
- Precision-Recall Curve
- Feature Importance plots
- Crash distribution visualizations
- <img width="567" height="455" alt="image" src="https://github.com/user-attachments/assets/e2ac2d87-7cdb-4b02-8461-885522ad4ec2" />
<img width="684" height="435" alt="image" src="https://github.com/user-attachments/assets/1e4c8d8d-942f-4b62-af9d-dbaa4170e263" />
<img width="576" height="455" alt="image" src="https://github.com/user-attachments/assets/31a86adc-8e63-4670-a3c4-1ac457fe25f9" />





  
---

## ⚠️ Limitations

- Performance varies on **rare crash scenarios**
- Model relies on **historical data only**
- Does not include real-time factors like traffic flow or driver behavior

---

## 💡 Recommendations

- Use the model to:
  - Identify **high-risk conditions**
  - Improve **road safety planning**
  - Allocate **emergency resources effectively**

- Future improvements:
  - Incorporate **real-time data**
  - Add **geospatial features**
  - Explore **advanced ensemble models**

---

## 🛠️ Tools & Technologies

### 🔹 Programming & Libraries
- Python
- pandas
- numpy
- scikit-learn
- xgboost
- imbalanced-learn (SMOTE)

### 🔹 Visualization
- matplotlib
- seaborn

### 🔹 Modeling Techniques
- Logistic Regression
- Random Forest
- XGBoost
- Stratified K-Fold Cross-Validation

### 🔹 Feature Engineering
- Interaction features
- Binning
- Encoding (Label Encoding)

---

## 🚀 Key Highlights

- ✔️ Handled **class imbalance effectively**
- ✔️ Improved minority class recall from **0.21 → 0.65**
- ✔️ Achieved **stable performance (cross-validated)**
- ✔️ Combined **technical rigor with business insight**

---

## 📌 Conclusion

This project demonstrates how machine learning can be applied to real-world safety problems. By progressively improving models and focusing on balanced performance, the final solution provides **meaningful insights into crash severity prediction**.

---

## 👤 Author
**David Wanyiri**

---

## ⭐ If you found this useful
Feel free to star the repo or share feedback!
