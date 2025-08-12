# Breast Cancer Prediction (BCP)
---

## Table of Contents
1. [Problem](#problem)  
2. [Objective](#objective)  
3. [Dataset](#dataset)  
4. [Methodology](#methodology)  
5. [Performance Summary](#performance-summary)  
6. [Results & Impact](#results--impact)  
7. [Conclusion](#conclusion)  
8. [Final Accuracy](#final-accuracy)  

---

## **Problem**
Breast cancer is caused by the uncontrolled growth of malignant cells in breast tissue, typically classified into **benign (non-cancerous)** or **malignant (cancerous)**.  
It is the **most common cancer** among women, accounting for nearly **1 in 3 diagnoses** in the United States, and is the **second leading cause of cancer-related deaths** in women.

---

## **Objective**
This project aims to **build and compare multiple supervised machine learning models** to predict whether a breast tumor is malignant (M) or benign (B).  
By analyzing medical patient data and tumor characteristics, the goal is to **empower medical professionals** with accurate, data-driven tools to assist in timely and effective decision-making.

---

## **Dataset**
- **Source:** [Kaggle - Breast Cancer Dataset](https://www.kaggle.com/datasets/yasserh/breast-cancer-dataset)  
- **Description:**
  - **Rows:** 569  
  - **Features:** 33 (including `id` and `diagnosis` as the target)  
  - **Target Variable:** `diagnosis` (M = Malignant, B = Benign)  
  - No missing or duplicate records.  
  - Tumor measurements provided for **Mean**, **Standard Error**, and **Worst Value**.  

| Feature | Description |
|---------|-------------|
| Radius | Distance from the center to the perimeter of the nucleus |
| Texture | Variation in pixel intensity in the nucleus image |
| Perimeter | Length of the nucleus boundary |
| Area | Pixel count inside the nucleus boundary |
| Smoothness | Variability of tumor edges |
| Compactness | (Perimeter² / Area) - 1.0 — ratio normalized |
| Concavity | Degree of inward curvature of the nucleus |
| Fractal dimension | Complexity (“roughness”) of the contour |

---

## **Methodology**
### **1. Data Preprocessing**
- Scaled numerical features.
- Encoded categorical variables.
- Applied **Train-Test Split** (80% train, 20% test).

### **2. Data Analysis**
- Generated statistical summaries.
- Created visualizations to understand distributions, correlations, and feature importance.

### **3. Machine Learning Models**
- **Logistic Regression**  
- **Support Vector Machine (SVM)**  
- **Naive Bayes**  
- **K-Nearest Neighbors (KNN)**  
- **Decision Tree**  
- **Random Forest**

### **4. Model Evaluation**
Metrics used:
- **Accuracy**
- **Precision**
- **Recall**
- **F1-score**
- **AUC-ROC Curve**

---

## **Performance Summary**
| Model | Accuracy | AUC ROC |
|-------|----------|---------|
| **Logistic Regression** | **0.974** | **0.997** |
| SVM | 0.965 | 0.994 |
| Naive Bayes | 0.956 | 0.992 |
| KNN | 0.956 | 0.973 |
| Decision Tree | 0.920 | 0.918 |
| Random Forest | 0.956 | 0.992 |

---

## **Results & Impact**
- **Best Model:** Logistic Regression (Tuned) – **97.4% accuracy**.
- Only **1 false negative** detected – critical for cancer detection.
- **Metrics for Logistic Regression:**
  - Training Accuracy: 0.989  
  - Testing Accuracy: 0.974  
  - Precision: 0.955  
  - Recall: 0.977  
  - F1-score: 0.974  

- **Hyperparameter Tuning:**  
  Optimized with **GridSearchCV** (10-fold CV) testing multiple:
  - C values (regularization strength)
  - Penalty types (L1, L2)
  - Solvers (liblinear, lbfgs)  
  → Achieved similar accuracy to baseline, indicating **default parameters were already near-optimal**.

- **Feature Importance:** Identified top predictors using model coefficients.

- **Second-Best Model:** SVM (96.4% accuracy).

---

## **Conclusion**
The **Breast Cancer Prediction Model** demonstrates:
- **Early & Accurate Diagnosis** capability.
- **Improved treatment effectiveness** by reducing false negatives.
- Reliable algorithm comparison for medical decision support.
- Proof that **data-driven healthcare** can save lives and raise care standards.

---

## **Final Accuracy**
 **97.4% (Logistic Regression – Tuned)**

---

## 📌 **More Info**
- **GitHub:** [YoussefEl-Hendawy](https://github.com/YoussefEl-Hendawy)  
- **LinkedIn:** [Youssef El Hendawy](https://www.linkedin.com/in/youssef-el-hendawy-7012b43)  
