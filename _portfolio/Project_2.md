---
title: "Early Patient Readmission Prediction"
collection: Projects
permalink: /portfolio/Project_2
excerpt: 'Developed a machine learning pipeline to predict early patient readmissions using a decade of clinical records from 130 US hospitals. Extensive data preprocessing was performed, class imbalance was addressed using SMOTE, and multiple models including Logistic Regression and Random Forest were evaluated, achieving the highest accuracy of 62.2%. Visualization techniques such as ROC curves and confusion matrices were used to assess model performance.'
#slidesurl: 'http://academicpages.github.io/files/slides1.pdf'
#paperurl: 'http://academicpages.github.io/files/paper1.pdf'
#citation: 'Your Name, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal 1</i>. 1(1).'
---


## Introduction

Hospital readmissions, especially early readmissions within 30 days of discharge, are a significant concern in healthcare management. Readmissions not only indicate potential shortcomings in post-discharge care but also contribute to increased healthcare costs. Predicting early readmissions can help hospitals improve patient care, allocate resources more effectively, and reduce operational costs. In this project, the objective is to leverage machine learning models to predict whether a patient will be readmitted within 30 days of discharge, based on historical clinical data.

The dataset used in this project comprises a decade's worth of clinical records from 130 US hospitals, containing patient demographic details, admission history, diagnostic codes, and medication information. A total of 101,766 records representing 71,518 unique patients are analyzed. The project focuses on transforming the raw dataset into a format suitable for predictive modeling through various data preprocessing techniques, including handling missing data, removing duplicates, and categorizing diagnostic codes.

Several machine learning models are implemented to predict patient readmission, including Logistic Regression, Random Forest, Support Vector Machines (SVM), and Gradient Boosting, among others. By applying Synthetic Minority Over-sampling Technique (SMOTE) to address class imbalance, the models are trained and evaluated based on their accuracy and F1-score. Visualization techniques, such as ROC curves and confusion matrices, are used to evaluate the performance of each model.

The ultimate goal of this project is to determine the most effective machine learning model for predicting early patient readmissions, which can be applied in hospital systems to optimize patient outcomes and resource allocation.


## Data Preprocessing

### 1. Removing Duplicate Records
- The dataset contains duplicate entries based on patient numbers (`patient_nbr`). To maintain data integrity, these duplicates are removed, ensuring each patient is represented only once.

### 2. Handling Missing Data
- Columns with a high proportion of missing values, such as `weight`, `payer_code`, and `medical_specialty`, are dropped.
- Missing values in the `race` column are imputed using the most frequent race category.

### 3. Removing Uninformative Features
- Irrelevant features, including `encounter_id`, `patient_nbr`, and highly imbalanced columns (where over 98% of the values are the same), are removed to optimize classification.

### 4. Categorizing Diagnostic Features
- The diagnostic columns (`diag_1`, `diag_2`, `diag_3`) are categorized using ICD-9 codes, improving interpretability.

### 5. Mapping Admission, Source, and Discharge Categories
- Admission types, admission sources, and discharge types are replaced with descriptive categories, consolidating similar meanings into one category (e.g., mapping ‘Urgent’ to ‘Emergency’).

### 6. Handling Age Feature
- Age ranges are converted into numerical values, with each range assigned a numeric value to correlate with the likelihood of readmission.

### 7. Removing Outliers
- Outliers in numeric columns are removed based on boxplot analysis to ensure consistency.

### 8. Handling Drug Medication Features
- Drug-related features with imbalanced distributions are dropped.

### 9. Transforming Glucose Serum Levels
- The `max_glu_serum` feature is mapped to numeric values: `None` (0), `Norm` (1), `>200` (2), and `>300` (2).

### 10. Handling Diabetes Medication
- The `diabetesMed` column is converted to numeric values: `No` (0) and `Yes` (1), due to its observed correlation with readmission rates.

### 11. Change of Medications
- The `change` column is transformed into numeric: `No` (0) and `Yes` (1), reflecting the impact of medication changes on readmission rates.

### 12. Target Variable Transformation
- The target variable (`readmitted`) is mapped to numeric values: `NO` (0), `>30` (1), and `<30` (2).

### 13. Categorical Feature Encoding
- One-hot encoding is applied to transform categorical features into numeric format.

### 14. Addressing Class Imbalance
- SMOTE (Synthetic Minority Over-Sampling Technique) is applied to balance the class distribution, improving the generalization and prediction capabilities of the model.

### 15. Data Split
- The dataset is split into training and testing sets, with 10% allocated for testing purposes.

## Model Accuracy Analysis

Multiple machine learning models were evaluated using training and testing accuracy, and F1 scores (micro). The results are summarized below:

| Model                  | Training Accuracy | Testing Accuracy | F1-Score (Micro) |
|------------------------|-------------------|------------------|------------------|
| Logistic Regression     | 0.634             | 0.622            | 0.622            |
| Decision Tree           | 0.638             | 0.572            | 0.572            |
| K Nearest Neighbor      | 0.719             | 0.546            | 0.546            |
| Naive Bayes             | 0.576             | 0.531            | 0.531            |
| Support Vector Machine  | 0.675             | 0.617            | 0.617            |
| Random Forest           | 0.785             | 0.612            | 0.612            |
| Gradient Boosting       | 0.736             | 0.609            | 0.608            |
| Bagging Classifier      | 0.689             | 0.604            | 0.604            |
| Adaboost Classifier     | 0.775             | 0.589            | 0.589            |

## Visualization & Evaluation

### 1. ROC Curves and AUC
ROC curves and AUC (Area Under Curve) values were used to assess the ability of each model to correctly classify instances across different classes.

### 2. Confusion Matrix
A heatmap of the confusion matrix was used to visualize the model’s effectiveness by showing counts of correctly and incorrectly predicted instances.

### 3. Bar Plots
Two bar plots were generated:
- One demonstrating the testing accuracy for each model.
- One illustrating F1 scores for each model.

## Conclusion
From the testing accuracy and F1-score comparisons, it was observed that Logistic Regression, Support Vector Machine (SVM), Random Forest, Gradient Boosting, and Bagging Classifier outperformed Decision Tree, KNN, Naive Bayes, and Adaboost Classifier. The best accuracy achieved was 0.622, with Logistic Regression performing the best overall.

