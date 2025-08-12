# Breast-Cancer-Prediction

## Table of Contents
1. [Problem](#problem)
2. [Objective](#objective)
3. [Dataset](#dataset)
4. [Methodology](#methodology)
5. [Results & Impact](#results--impact)
6. [Conclusion](#conclusion)
7. [Final Accuracy](#final-accuracy)
8. [More Info](#for-more-info)
    
## **Problem**
Breast cancer is the growth of malignant cells in the breast, with two types: **benign** or **malignant**.It is the most common cancer affecting women and accounts for nearly 1 in 3 cancers diagnosed among women in the United States. It is also the second leading cause of cancer-related deaths among women.

## **Objective**
The goal of this project is to build and compare several supervised machine learning models to predict whether a breast tumor is malignant (M) or benign (B).  
Through medical analysis of patient data and tumor characteristics, the project aims to empower medical professionals with essential information for making trusted decisions about patient care.

## **Dataset**
- **Source:** Breast cancer dataset from Kaggle: [Link](https://www.kaggle.com/datasets/yasserh/breast-cancer-dataset)
- **Description:**
  1. A total of 33 feature columns, including "ID", with `diagnosis` as the target variable.
     
     | Feature | Description |
     |---------|-------------|
     | Radius | Distance from the center to the perimeter of the nucleus. |
     | Texture | Variation in pixel intensity in the nucleus image. |
     | Perimeter | Length of the boundary of the nucleus. |
     | Area | Number of pixels inside the nucleus boundary. |
     | Smoothness | Variability in the smoothness of tumor edges. |
     | Compactness | (Perimeter² / Area) - 1.0 — ratio of perimeter to area, normalized. |
     | Concavity | Degree to which the nucleus contour contains concave portions. |
     | Fractal dimension | Measure of the complexity of the contour (how “rough” it is). |
  2. The total number of observations is 569.
  3. Features for each tumor include **Mean**, **Standard Error**, and **Worst Values**.
  4. There are no duplicate or missing value rows in the dataset.

## **Methodology**
### **Data Preprocessing**
- Handled missing values.
- Scaled numerical features.
- Encoded categorical variables.
- Performed Train-Test Split (80% training, 20% testing) to evaluate model performance.

### **Data Analytics**
- Explored and understood the dataset using statistical summaries and visualization tools.

### **ML Models**
- Applied a range of supervised machine learning algorithms for prediction and evaluated them.

### **Performance Evaluation**
- Assessed models using metrics such as Accuracy, Precision, Recall, AUC-ROC, and F1-score.

| Model | Final Accuracy | AUC ROC |
|-------|----------------|---------|
| Logistic Regression | 0.970 | 0.997 |
| SVM | 0.965 | 0.994 |
| Naive Bayes | 0.956 | 0.992 |
| KNN | 0.956 | 0.973 |
| Decision Tree | 0.920 | 0.918 |
| Random Forest | 0.956 | 0.992 |

## **Results & Impact**
1. Compared multiple models based on performance metrics.
2. Identified and highlighted the best-performing algorithm for breast cancer classification.
3. The analysis indicates that the **Logistic Regression model (Tuned)** demonstrates the best performance (97.4%) for this dataset,  
   achieving a near-optimal result with only one false negative across all predictions — a highly significant result in cancer prediction.
   - Training Accuracy: 0.989
   - Testing Accuracy: 0.974
   - Precision: 0.955
   - Recall: 0.977
   - F1 Score: 0.974
4. **Hyperparameter Tuning**  
   - Optimized the Logistic Regression model using **GridSearchCV** with 10-fold cross-validation.  
   - Tested multiple values of regularization strength (C), penalty type (L1, L2), and solver (liblinear, lbfgs).  
   - The best hyperparameters were applied to the test set, achieving accuracy similar to the baseline, indicating that the default parameters were already near-optimal.  
   - Analyzed feature importance by ranking the model coefficients to highlight the most influential predictors.
5. SVC also performed well, ranking second with a final accuracy of 96.4%.

## **Conclusion**
The Breast Cancer Prediction (BCP) model aims to:
- Enable early and accurate diagnoses.
- Significantly improve treatment effectiveness and patient outcomes.
- Deliver a reliable machine learning model for accurate tumor classification.
- Provide insights into the most effective algorithms for this dataset.
  
This project demonstrates the life-saving potential of data-driven medical analysis and highlights its transformative role in improving healthcare standards and addressing critical real-world health challenges.

## **Final Accuracy**
**97.4% (Logistic Regression – Tuned)**

## **For More Info**
- **LinkedIn:** [Youssef El-Hendawy] (www.linkedin.com/in/youssef-el-hendawy-7012b4325)
