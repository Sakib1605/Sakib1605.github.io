---
title: "Machine Learning Project: Movie Recommendation & Insights Analysis"
collection: Projects
permalink: /portfolio/Project_3
excerpt: 'Utilized natural language processing (NLP) and machine learning techniques to extract valuable insights from a movie dataset. Developed a content-based movie recommendation system that suggests films based on similarities in movie descriptions, leveraging NLP to analyze and compare textual data. Implemented multilabel genre classification by analyzing movie overviews, enabling the categorization of films into multiple genres simultaneously. Additionally, predicted movie ratings using various features such as genre, budget, and revenue, applying machine learning methods and feature importance analysis.'
#slidesurl: 'http://academicpages.github.io/files/slides1.pdf'
#paperurl: 'http://academicpages.github.io/files/paper1.pdf'
#citation: 'Your Name, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal 1</i>. 1(1).'
---


## Introduction

With the plethora of movies available on the internet these days, viewers often face difficulty in finding movies that align with their interests. Relying entirely on genre-based searches may overlook individual preferences, highlighting the importance of content-based movie suggestions. By leveraging movie descriptions and plot summaries, content-based movie recommendation systems can facilitate the exploration of similar movies that match viewer preferences.

Moreover, genre classification based on movie plot descriptions facilitates efficient genre categorization by identifying frequently used words in movie descriptions or themes associated with genres. Accurate genre classification helps audiences find movies that align with their preferred genres.

Understanding audience preferences and gaining insights into factors influencing movie success is crucial in the film industry. This emphasizes the need for exploratory analysis and movie ratings prediction, which offers insights into key features contributing to a movie’s success and helps understand audience preferences.

The motivation behind this project lies in enhancing movie exploration and improving user satisfaction by suggesting more relevant movies, effectively categorizing movies into genres based on content, and uncovering key features associated with audience engagement.

## Problem Statement

The primary objective of the project is to employ natural language processing (NLP) and machine learning methods to derive meaningful insights from a movie dataset. The project comprises three tasks:

- **Content-based Movie Recommendation**: Develop a content-based recommendation system using NLP techniques to suggest movies based on similarities in movie descriptions. This involves analyzing movie descriptions and identifying semantic similarities.
  
- **Genre Classification Based on Movie Content**: Use NLP techniques to analyze textual content from movie overviews and develop classification models to categorize movies into multiple genres simultaneously. This is a multilabel classification problem.
  
- **Movie Ratings Prediction**: Predict movie ratings by analyzing features such as genre, budget, revenue, runtime, language, and production companies. Conduct feature importance analysis to identify key factors impacting movie ratings.

## Method

### 3.1 Dataset Information and Preprocessing

- **Dataset**: Data on 50 movies with 26 feature columns was initially extracted via web scraping from IMDb. This data was merged with a publicly available movie dataset from Kaggle, resulting in a final dataframe of 432,410 movies with 20 feature columns.

- **Preprocessing Steps**:
  1. **Handling Duplicate Movie Names**: Removed duplicate entries to ensure unique representation of each movie.
  2. **Handling Missing Values**: Removed columns with high percentages of missing values and imputed missing values for some categorical columns.
  3. **Data Type Conversion**: Converted columns to appropriate data types for consistency in analysis.
  4. **Handling Outliers**: Removed movies with unusual runtimes.
  5. **Feature Extraction**: Extracted release year and month from the release date.
  6. **One-hot Encoding for Genres**: Applied one-hot encoding to convert genre categories into binary features.
  7. **Text Preprocessing**: Preprocessed movie overviews by removing punctuation, eliminating stop words, and converting text to lowercase.
  8. **Removing Unnecessary Columns**: Removed irrelevant columns for movie ratings prediction.
  9. **Scaling Numerical Features**: Scaled numerical features to prevent feature dominance.

### 3.2 Modelling

- **Movie Recommendation System**:
  - **Word2Vec Approach**: Utilized word embeddings to capture semantic relationships. Combined "title," "overview," and "genre" columns into a "content" column, trained the Word2Vec model, and calculated cosine similarity to recommend similar movies.
  
  - **TF-IDF Approach**: Used TF-IDF vectorization to convert text data into numerical vectors. Calculated cosine similarity to suggest top 10 similar movies.

- **Movie Genre Classification**:
  - Applied preprocessing techniques to movie content text data, converted text into numerical vectors using TF-IDF, and trained classification models such as Logistic Regression, Random Forest, Gradient Boosting, and Adaboost Classifier. Evaluated models using precision, recall, and f1-score.

- **Movie Ratings Prediction**:
  - Trained various regression models including Linear Regression, Ridge Regression, Support Vector Regressor, Decision Tree Regressor, Random Forest, Extreme Gradient Boosting, and Bagging Regressor. Evaluated model performance using MSE and MAE, and conducted feature importance analysis.

## Results and Discussion

### 4.1 Results for Exploratory Data Analysis

- **Genre Analysis**:
  - Distribution of movie counts across genres shows Drama, Documentary, and Comedy as the most prevalent genres.
  - Most common words in movie descriptions vary by genre, providing insights into content variations.
  - Co-occurrences of genres reveal patterns such as Action movies frequently co-occurring with Drama and Adventure.

- **Rating Analysis**:
  - Documentary and Animation genres receive higher average ratings from 2010 to 2023.

- **Revenue Analysis**:
  - Average revenue for certain genres decreased from 2021 to 2022, with increases in genres like Action and Adventure.

- **Runtime Analysis**:
  - Movies with runtimes between 120-180 minutes have the highest average popularity.

- **Movie Language Analysis**:
  - English is the most prevalent language in the dataset.

- **Popularity Analysis**:
  - Adventure is the most popular genre in 2023.

### 4.2 Machine Learning Results

- **Movie Recommendation System Results**:
  - Both Word2Vec and TF-IDF approaches effectively recommend movies similar to the selected movie based on content and genre.

- **Genre Classification Results**:
  - Logistic Regression performed well for certain genres, while Random Forest and Gradient Boosting also showed effective results for specific genres. Adaboost Classifier had moderate performance.

- **Movie Ratings Prediction Results**:
  - Ensemble methods like Random Forest, Gradient Boosting, and Bagging Regressor outperformed individual models. Feature importance analysis identified rating count, runtime, release year, and popularity as significant factors affecting movie ratings.

## Conclusion

The project successfully employed NLP and machine learning techniques to address challenges in movie recommendations, genre classification, and ratings prediction. Key contributions include enhanced movie discovery, effective content categorization, and valuable audience insights. This project improves movie exploration, categorization, and understanding of factors influencing movie success.

## References

[1] Asaniczka. (2023). TMDB Movies Dataset. Retrieved from: [Kaggle TMDB Movies Dataset](https://www.kaggle.com/datasets/asaniczka/tmdb-movies-dataset-2023-930k-movies)
