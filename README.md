# 🔍 Hybrid Resampling for Imbalanced Data

A Comparative Study of SMOTE, Tomek Links, LSSA+SMOTE, and Graph KNN+SMOTE with SVM  
**Author:** Gobikrishnan V.S  
**Guide:** Dr. S. Jayachandran  
**Affiliation:** Department of Data Science, SASTRA Deemed University, Chennai

---

## 📌 Overview

This project investigates the effectiveness of multiple hybrid resampling techniques in handling **imbalanced datasets**—specifically for **credit card fraud detection**. The study evaluates seven experimental setups using **Support Vector Machine (SVM)** as the core classifier and applies resampling techniques like **SMOTE**, **Tomek Links**, **LSSA**, and the proposed **Graph KNN-SMOTE**.

---

## 🧠 Techniques Compared

1. **SVM (No Preprocessing)**  
2. **SVM (With Preprocessing)**  
3. **SMOTE** (Synthetic Minority Oversampling Technique)  
4. **Tomek Links**  
5. **LSSA** (Levy Sparrow Search Algorithm)  
6. **LSSA + SMOTE**  
7. **Graph KNN-SMOTE** ✅ *Best Performing*

---

## 📊 Dataset

- **Name**: `card_transdata.csv`
- **Source**: [Kaggle](https://www.kaggle.com/code/marcinrutecki/best-techniques-and-metrics-for-imbalanced-dataset?select=card_transdata.csv)
- **Size**: 1,000,000 transactions
- **Target Variable**: `fraud` (0 = Not Fraud, 1 = Fraud)
- **Important Features**:
  - `distance_from_home`, `distance_from_last_transaction`
  - `used_chip`, `used_pin_number`

---

## 🧪 Experimental Setup

Each technique was evaluated with:
- **Support Vector Machine (RBF kernel)**
- **Feature Standardization**
- **Custom Feature Engineering & Cleaning**

---

## 📈 Performance Comparison

| Method               | Accuracy | Precision | Recall | F1-Score | RMSE  |
|----------------------|----------|-----------|--------|----------|--------|
| SVM (No preprocessing) | 0.915    | 0.574     | 0.175  | 0.268    | 0.291  |
| SVM (Preprocessing)    | 0.977    | 0.985     | 0.858  | 0.760    | 0.149  |
| SMOTE                 | 0.991    | 0.982     | 0.999  | 0.990    | 0.097  |
| Tomek Link            | 0.993    | 0.986     | 0.933  | 0.959    | 0.086  |
| LSSA                  | 0.938    | 0.591     | 0.964  | 0.729    | 0.249  |
| LSSA + SMOTE          | 0.916    | 0.888     | 0.952  | 0.919    | 0.290  |
| **Graph KNN-SMOTE**   | **0.945**| **0.901** | **0.999**| **0.948**| **0.235** |

✅ **Graph KNN-SMOTE** offered the best trade-off between high recall and low false negatives, making it most suitable for fraud detection.

---

## 🔍 Key Insights

- **Preprocessing alone** significantly boosts performance but does not address class imbalance completely.
- **SMOTE** improved recall but introduced synthetic noise, increasing false positives.
- **Tomek Link** gave the best precision but lower recall.
- **LSSA** optimized hyperparameters but required high computational cost.
- **Graph KNN-SMOTE**, a geometry-aware oversampling method, yielded the most balanced and robust results with **F1-score: 0.948**.

---

## 🧰 Tools & Libraries Used

- Python
- Pandas, NumPy
- Scikit-learn
- Imbalanced-learn
- Matplotlib, Seaborn

---

## 🔮 Future Work

- Apply **cost-sensitive learning** to reflect real-world misclassification costs.
- Introduce **adaptive resampling** based on data density and fraud pattern evolution.
- Experiment with **deep learning** and **ensemble-based meta classifiers**.
- Extend to **multi-class imbalance** scenarios.

---

## 🧑‍💼 Author

**Gobikrishnan V.S**  
M.Sc. Data Science, SASTRA Deemed University  
📫 Email: gobiventhan@gmail.com

---

