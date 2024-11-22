---
title: "Statistical Learning Project using R: Case study of Pima Indian Diabetes Dataset"
collection: Projects
permalink: /portfolio/Project_8
excerpt: 'Designed a plant disease diagnosis system using Gemini-Vision-Pro for extracting visual features and generating symptom descriptions from images. Integrated these insights with a multi-modal fusion model to compare symptom based and image-based classification methods, improving classification accuracy.'
slidesurl: 'https://github.com/Sakib1605/Case_study_Pima_Indian_Diabetes_Dataset/blob/main/STAT_6801_FINAL_PROJECT.pdf'
#paperurl: 'http://academicpages.github.io/files/paper1.pdf'
#citation: 'Your Name, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal 1</i>. 1(1).'
---

[Github_Repository_Link](https://github.com/Sakib1605/Case_study_Pima_Indian_Diabetes_Dataset)

## Abstract
The primary objective of this project is to evaluate the effectiveness of various classification models in predicting diabetes outcomes using the Pima Indian Diabetes dataset. By comparing performance metrics such as accuracy, precision, recall, and area under the ROC curve (AUC), the project provides a comprehensive assessment of different models. The analysis also identifies key variables impacting the outcome. A two-level ensemble approach, where a combination of Generalized Linear Model (GLM), Generalized Additive Model (GAM), Support Vector Machine (SVM), and Random Forest feeds into a Neural Network for final predictions, achieved the highest accuracy (99%) on the test dataset.

## Introduction
Diabetes is a chronic disease characterized by high blood sugar due to either insufficient insulin production or ineffective insulin utilization. The Pima Indian Diabetes dataset allows investigation into key demographic and health-related characteristics, offering insights into effective diabetes risk minimization approaches.

## Dataset Description
The dataset is derived from a study by the National Institute of Diabetes and Digestive and Kidney Disease. It contains health characteristics of 768 adult female Pima Indians, with the aim of detecting key factors influencing diabetes.

### Features:
- **Pregnant**: Number of pregnancies.
- **Glucose**: Plasma glucose concentration at 2 hours.
- **Diastolic**: Diastolic blood pressure (mmHg).
- **Triceps**: Triceps skinfold thickness (mm).
- **Insulin**: Two-hour serum insulin (mu U/ml).
- **BMI**: Body mass index.
- **Diabetes Pedigree**: Probability of diabetes based on family history.
- **Age**: Age in years.
- **Test Outcome**: Binary outcome for diabetes (1 = diabetic, 0 = non-diabetic).

## Data Pre-processing
- **Handling Unrealistic Values**: Zero values in glucose, diastolic, triceps, insulin, and BMI were replaced with NA.
- **Missing Values**: Imputed using the median of the respective column.
- **Outliers**: Box plots were used to detect and handle outliers.
- **Feature Importance**: Correlation analysis was performed to assess relationships among variables.
- **Scaling**: Numeric features were scaled to standardize the dataset.
- **Data Split**: 100 cases were assigned to the test set, and the remaining data were used for training.

## Model Analysis

### Generalized Linear Model (GLM)
GLMs use logistic regression to predict the binary outcome. Initially, all features were used to train the model, but the stepwise AIC variable selection method was applied to prevent overfitting, improving performance.

### Generalized Additive Model (GAM)
GAMs allow flexibility by using smooth functions to capture non-linear patterns. All features were used to train the GAM.

### Decision Trees and Random Forest
A decision tree was trained, and cross-validation was used to select the optimal tree size. Pruning was applied to simplify the tree. Random Forest, an ensemble approach combining predictions of multiple trees, was also trained.

### Support Vector Machine (SVM)
Both linear and radial SVM models were applied. The radial SVM, offering a flexible decision boundary, showed better performance than the linear SVM.

### K-Nearest Neighbor (KNN)
KNN was trained on the scaled data, and hyperparameter tuning was applied to optimize performance.

### Neural Networks
- **Unscaled Data**: A neural network with two hidden layers was trained on the unscaled data.
- **Scaled Data**: A neural network with 10 hidden layers was trained on the scaled data, which resulted in better performance.

### Two-Level Ensemble Approach
The first level included GLM, GAM, SVM, KNN, and Random Forest. Their predictions were used as inputs to a Neural Network in the second level. This approach achieved the highest accuracy.

### Majority Voting Ensemble
Predictions from GLM, GAM, SVM, KNN, Random Forest, and Neural Networks were combined using majority voting.

## Evaluation Metrics
- **Accuracy**: Measures the correct predictions over the total cases.
- **Confusion Matrix**: Provides true positives, true negatives, false positives, and false negatives.
- **Precision and Recall**: Precision measures the accuracy of positive predictions, while recall measures the model’s ability to identify positive cases.
- **ROC Curve**: Visual representation of the model’s ability to differentiate between classes, with AUC used to quantify performance.

## Results
| Model                       | Accuracy | False Positive Rate | False Negative Rate | Precision | Recall | AUC   |
|-----------------------------|----------|---------------------|---------------------|-----------|--------|-------|
| Generalized Linear Model     | 0.76     | 0.076               | 0.542               | 0.923     | 0.759  | 0.6901|
| Random Forest                | 0.98     | 0.0153              | 0.0286              | 0.9846    | 0.9846 | 0.978 |
| Two-Level Ensemble           | 0.99     | 0                   | 0.0286              | 1         | 0.9848 | 0.9857|

## Conclusion
The two-level ensemble approach proved to be the most effective model, achieving 99% accuracy. Random Forest also performed well with 98% accuracy. Feature scaling played a significant role in improving the performance of the neural network model. The analysis showed that glucose is the most significant predictor for diabetes, followed by BMI and age.

## References
1. World Health Organization, Diabetes [accessed on 2023] Retrieved from: [WHO](https://www.who.int/health-topics/diabetes#tab=tab_1).
2. Benarbia, Meriem, "A Machine Learning Approach to Predicting the Onset of Type II Diabetes in a Sample of Pima Indian Women" (2022). CUNY Academic Works.
3. Abedini, M., Bijari, A., and Banirostam, T. (2020). Classification of Pima Indian diabetes dataset using ensemble models. Ijarcce, vol. 9, no. 7, pp. 1–4.
4. Dataset: [Pima Indians Diabetes Database](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database).
