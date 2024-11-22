---
title: "Neural Network Project: Symptom Driven Plant Disease Classification"
collection: Projects
permalink: /portfolio/Project_6
excerpt: 'Designed a plant disease diagnosis system using Gemini-Vision-Pro for extracting visual features and generating symptom descriptions from images. Integrated these insights with a multi-modal fusion model to compare symptom based and image-based classification methods, improving classification accuracy.'
slidesurl: 'https://github.com/Sakib1605/Symptom_Driven_Plant_Disease_Classification/blob/main/CIS_6050_Neural_Network_Project_Report.pdf'
#paperurl: 'http://academicpages.github.io/files/paper1.pdf'
#citation: 'Your Name, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal 1</i>. 1(1).'
---
[Github_Repository_Link](https://github.com/Sakib1605/Symptom_Driven_Plant_Disease_Classification)


## Abstract
This project presents a novel approach to plant disease diagnosis by combining image-based classification with predictive symptom analysis. By leveraging both visual and textual features, the approach moves beyond traditional image-only methods, providing a more comprehensive diagnostic tool. The multi-modal system incorporates four Convolutional Neural Network (CNN) models: VGG16, DenseNet, InceptionV3, and a custom-built CNN. DenseNet outperformed other models with a training accuracy of 95.5% and a validation accuracy of 85%. This approach enhances disease diagnosis and has significant potential for sustainable agriculture by providing effective tools for early detection.

## Introduction

### i. Motivation
Accurate identification of plant diseases is crucial for ensuring optimal crop yields, food security, and environmental sustainability. Traditional manual methods for diagnosing plant diseases are time-consuming and require expert knowledge. This project aims to automate plant disease classification by using both image and symptom data, leveraging advanced machine learning techniques like Convolutional Neural Networks (CNN) and large language models (LLMs). The goal is to enhance the field of automated plant health monitoring and management, with a specific focus on accurate symptom-driven disease identification.

### ii. Significance
The prevalence of plant diseases has increased due to changes in cultivation methods and inadequate protection measures. Automated methods for disease detection can significantly reduce the need for manual labor and improve monitoring efficiency. By integrating textual symptom descriptions with image analysis, this project provides a more robust tool for plant disease classification.

### iii. Potential Applications
The proposed system has practical applications in early disease detection, automated monitoring systems, and decision-making processes in agriculture. It offers the potential to reduce economic losses and promote sustainable crop management by providing timely disease diagnosis.

## Problem Statement
This project addresses the critical challenge of automating plant disease diagnosis by combining image and textual feature analysis. The objective is to classify plant diseases based on both visual features from plant images and textual symptom descriptions. This approach extends traditional methods that rely solely on images and aims to improve the reliability of disease classification.

## Methodology

### i. Dataset Information
Data for this project was obtained from multiple sources, including "Plant Village" (Hughes et al., 2015), Kaggle, and "Dataset for Crop Pest and Disease Detection" (Mensah et al., 2023). The dataset includes images of both healthy and diseased tomato plants, representing five classes: healthy, Leaf Blight, Leaf Curl, Septoria Leaf Spot, and Verticillium Wilt.

### ii. Data Pre-Processing
To enhance the diversity of training examples, image augmentation techniques such as scaling, rotation, and flipping were applied. The dataset was balanced across classes to ensure the model could generalize effectively.

### iii. Model Architecture
The project utilized CNN architectures, including pretrained models like VGG16, DenseNet, and InceptionV3, as well as a custom CNN. These models were used for image feature extraction, while a multi-modal fusion technique was employed to integrate textual symptom descriptions with the CNN output.

DenseNet emerged as the top-performing model, achieving a training accuracy of 95.5% and a validation accuracy of 85%. The fusion of image and text features allowed for more accurate disease classification compared to image-only methods.

### iv. Symptom Prediction
Gemini-Vision-Pro, a language model, was used to generate symptom descriptions from plant images. These descriptions were then integrated into the classification process using a multi-modal fusion approach.

## Evaluation

### i. Classification Accuracy
DenseNet demonstrated the best performance among the CNN models, achieving a training accuracy of 95.5% and a validation accuracy of 85% after 10 epochs. Evaluation metrics such as precision, recall, and F1-score were used to assess model performance.

### ii. Symptom Prediction Accuracy
Cosine similarity was used to compare generated symptoms with reference texts. The model performed well for diseases like Leaf Blight and Septoria Leaf Spot, achieving high similarity scores.

### iii. ROC-AUC Scores
All disease classes achieved ROC-AUC scores above 90%, indicating the model’s ability to distinguish between classes effectively.

## Results
DenseNet outperformed other CNN models in the multi-modal fusion architecture. The system’s accuracy was further enhanced by combining image features with symptom descriptions. The multi-modal approach achieved higher classification accuracy compared to image-only methods, even when using fewer images.

## Conclusion
The integration of image and textual data via multi-modal fusion improved the classification accuracy of plant disease diagnosis. DenseNet, in particular, showed strong performance with 95.5% training accuracy and 85% validation accuracy. The project demonstrates that combining image data with symptom descriptions offers a more reliable and comprehensive method for plant disease diagnosis. Future work could explore incorporating external factors like weather and geographical data to further enhance disease classification.

## References
- Hughes, David and Salathé, Marcel. "An open access repository of images on plant health to enable the development of mobile disease diagnostics." arXiv preprint arXiv:1511.0800.
- Mensah, Kwabena Patrick, et al. "Dataset for Crop Pest and Disease Detection." Mendeley Data, 2023.
- Alsakar, Yasmin M., et al. "Plant disease detection and classification using machine learning and deep learning techniques: Current trends and challenges." World Conference on Internet of Things, 2023.
