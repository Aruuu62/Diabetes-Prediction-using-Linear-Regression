# Diabetes Prediction using Linear Regression

This project demonstrates how to use **Linear Regression** for predicting the presence of diabetes based on medical attributes. Although Linear Regression is traditionally a regression technique, we adapt it here for binary classification by rounding predicted values to 0 or 1.

---

## 📊 Dataset Overview

The dataset (`diabetes.csv`) contains 768 entries, each representing a patient, with 8 features and 1 target:

**Features:**
- Pregnancies
- Glucose
- BloodPressure
- SkinThickness
- Insulin
- BMI
- DiabetesPedigreeFunction
- Age

**Target:**
- Outcome (1 = Diabetic, 0 = Non-diabetic)

---

## 🧹 Data Preprocessing

To ensure cleaner data for modeling, the following steps were performed:

- **Zero Replacement:**  
  Replaced all zero values in `Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, and `BMI` with the **median** of each respective column.

- **Special Adjustments:**
  - Replaced the **first row’s Glucose** with the **maximum** glucose value from the dataset.
  - For rows with the **minimum age**, their **Glucose** values were updated to the **minimum** in the column.

---

## 🔍 Model Description

- **Algorithm:** Linear Regression (from `sklearn`)
- **Classification Trick:** Predictions were rounded to the nearest integer to convert continuous output into binary classification (0 or 1).
- **Train-Test Split:** 80% for training, 20% for testing.

---

## 📈 Evaluation Metrics

The model’s performance was evaluated using standard classification metrics:

| Metric     | Value     |
|------------|-----------|
| Accuracy   | 0.760     |
| Precision  | 0.680     |
| Recall     | 0.618     |
| F1 Score   | 0.648     |

**Confusion Matrix:**
