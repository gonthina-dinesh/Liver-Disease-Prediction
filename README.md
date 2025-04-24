# 🩺 Liver Disease Stage Prediction

This project builds a machine learning model to predict the **stage of liver cirrhosis** based on clinical data. It uses a Random Forest Classifier and includes preprocessing, feature engineering, training, and evaluation.

---

## 📌 Objective

Predict the **histologic stage of liver cirrhosis** (1, 2, or 3) using patient clinical records from a Mayo Clinic study.

---

## 📁 Dataset Overview

- Source: Mayo Clinic PBC study (1974–1984)
- Records: 25,000 patients
- Target: `Stage` (1, 2, or 3)
- Sample features:
  - Demographics: `Age`, `Sex`
  - Symptoms: `Ascites`, `Spiders`, `Edema`
  - Lab values: `Bilirubin`, `Albumin`, `Cholesterol`, `SGOT`, `Platelets`, etc.
  - Status: `C` (censored), `CL` (transplant censored), `D` (death)

---

## 🛠️ Preprocessing

- **Encoding**: One-hot encoded categorical columns (e.g., `Sex`, `Status`, `Drug`)
- **Train-Test Split**:
  - Training: 16,000 samples
  - Validation: 4,000 samples
  - Testing: 5,000 samples
- **Features**: Combined numeric and one-hot encoded features

---

## 🤖 Model

- Algorithm: `RandomForestClassifier (random_state=42)`
- Trained on numerical + encoded categorical columns

---

## 📊 Evaluation

| Dataset    | Metric               | Value     |
|------------|----------------------|-----------|
| Training   | MSLE                 | 0.00093   |
| Validation | MSLE                 | 0.01078   |
| Testing    | RMSLE                | 0.09209   |
| Validation | Accuracy             | **95.08%** |
| Testing    | Accuracy             | **95.78%** |

---

## ✅ Conclusion

This system accurately predicts liver cirrhosis stages using both symptoms and lab results. The high accuracy makes it a useful model for early diagnosis and clinical decision support.

---
