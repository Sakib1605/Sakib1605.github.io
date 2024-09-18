---
title: "Analysis of Big Data Project: Exploratory Data Analysis using PySpark"
collection: Projects
permalink: /portfolio/Project_3
excerpt: 'Utilized PySpark for comprehensive Exploratory Data Analysis (EDA) on US Census data spanning from 2015 to 2017. Employed advanced visualization techniques to explore demographic attributes, including ethnic composition and gender distribution. Investigated socioeconomic factors such as poverty rates, employment patterns, income disparities, and commute patterns across different states to analyze temporal trends for comprehensive insights.'
#slidesurl: 'http://academicpages.github.io/files/slides1.pdf'
#paperurl: 'http://academicpages.github.io/files/paper1.pdf'
#citation: 'Your Name, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal 1</i>. 1(1).'
---

[Github_Repository_Link](https://github.com/Sakib1605/Exploratory_Data_Analysis_using_PySpark)

## 1. Introduction

This report documents the steps taken for an exploratory data analysis (EDA) on the "US Census Demographic Data" using PySpark. The dataset provides insights into the demographic and socio-economic characteristics of different population groups, including variables such as gender, race/ethnicity, income, employment status, and poverty rates.

The primary objective of the analysis is to explore socio-economic disparities across different demographic groups, identify trends in employment and income, and understand how various factors are interrelated. PySpark was chosen due to its ability to efficiently process large datasets distributed across multiple nodes, making it ideal for handling census-scale data.

---
## 2. Dataset Description

The dataset used in this analysis is sourced from the U.S. Census Bureau and contains detailed demographic and socio-economic information on various population groups across the United States. The dataset includes the following key variables:

- **Age:** Numerical variable representing the age of individuals.
- **Gender:** Categorical variable representing the gender of individuals (Male, Female).
- **Race/Ethnicity:** Categorical variable representing the race or ethnicity of individuals.
- **Income:** Numerical variable representing the annual income of individuals.
- **Employment Status:** Categorical variable indicating whether an individual is employed, unemployed, or not in the labor force.
- **Poverty Status:** Categorical variable indicating whether an individual is below the poverty line.

The dataset is extensive and covers a large population sample, making it well-suited for identifying trends and performing detailed analysis on socio-economic conditions across the country. Due to the large size of the data, PySpark was used for efficient distributed processing. The data was loaded into a PySpark DataFrame, leveraging PySpark’s distributed computing capability. Given the large size of census data, PySpark allows for optimized data loading and transformation, reducing processing time. Efficient data loading is critical in ensuring that subsequent analysis is performed smoothly on large-scale datasets.

---

## 3. Data Cleaning

Data cleaning was a crucial step in ensuring the reliability and accuracy of the analysis. The following tasks were performed during the cleaning phase:

- **Handling Missing Values:** Missing data in key variables such as income and employment status were identified. Missing values were either imputed based on logical assumptions or removed from the dataset when they could distort the analysis.
- **Data Type Adjustments:** To ensure proper analysis, categorical and numerical data types were corrected. For instance, income and age were formatted as numeric types, while gender and employment status were treated as categorical variables.

By cleaning the data, we ensured that the dataset was accurate and ready for meaningful exploration without the risk of misinterpreting results due to data quality issues.

---

## 4. Exploratory Data Analysis (EDA)

### 4.1 Summary Statistics
The analysis began by generating summary statistics to understand the distribution of key variables such as income, age, and employment status. Summary statistics helped identify the central tendencies (mean, median) and variabilities (standard deviation) within the data. Summary statistics provide a foundational understanding of the data, highlighting any extreme values (outliers) and ensuring that the distributions of variables are understood before proceeding with more detailed analysis.

---

### 4.2 Income Distribution Analysis
Income distribution was one of the primary focuses of the analysis. The goal was to examine the spread of income across the population, identifying which income brackets had the most individuals. The analysis revealed that a significant portion of the population was concentrated in lower income ranges, suggesting income inequality. Understanding income distribution is essential for analyzing economic disparities. Identifying income brackets with a high concentration of individuals can inform policies aimed at addressing poverty and promoting economic equity.

**Findings:** The analysis showed a skewed income distribution, with a heavy concentration of individuals in lower income ranges, indicating potential economic inequality across the population.

---

### 4.3 Gender and Employment Status Analysis
A comparative analysis of employment status across gender groups was conducted. The goal was to examine whether significant disparities existed in employment rates between males and females. Gender-based analysis helps in identifying socio-economic gaps that may exist in the workforce. By analyzing employment status across genders, we aimed to uncover potential imbalances in job opportunities and participation rates.

**Findings:** The results indicated that females had lower employment rates compared to males, highlighting gender disparities in labor force participation. This finding suggests potential barriers for women in the workforce, which could be further explored in future analyses.

---

### 4.4 Regional Employment Variations
Employment rates were also analyzed by geographic region to understand whether employment opportunities were evenly distributed across different parts of the country. Regional analysis provides insights into geographic inequalities in employment. Identifying regions with higher unemployment rates can help policymakers target those areas for job creation and economic development initiatives.

**Findings:** The analysis revealed regional disparities, with certain areas experiencing higher unemployment rates. These variations suggest that labor market conditions are not uniform across the country and that some regions face more economic challenges than others.

---

### 4.5 Age and Income Correlation
The relationship between age and income was examined to understand how income levels change across different age groups. This analysis aimed to determine whether older individuals, who typically have more work experience, tend to have higher incomes compared to younger individuals. Analyzing the relationship between age and income helps reveal trends in earning potential over a lifetime. It can indicate whether individuals are reaching their peak earning years later in life or whether younger generations face economic challenges in securing high-paying jobs.

**Findings:** The analysis showed that income generally increased with age, particularly in mid-life (ages 35-50), which is consistent with the idea that earning potential rises with experience. However, income started to decline in older age groups (over 60), likely due to retirement and reduced labor market participation.

---

### 4.6 Poverty Rate by Demographic Groups
The final analysis focused on the poverty rate across various demographic groups, including race/ethnicity and gender. This analysis aimed to identify which groups were most vulnerable to poverty. Analyzing poverty rates by demographic group helps uncover socio-economic inequalities that affect specific communities. Identifying vulnerable groups can inform social welfare policies aimed at reducing poverty and improving living standards.

**Findings:** The analysis revealed that certain minority groups had disproportionately higher poverty rates compared to others, indicating significant economic inequality. Women also had higher poverty rates compared to men, further emphasizing gender disparities in economic well-being.

---

## 5. Conclusion

The exploratory data analysis using PySpark provided critical insights into socio-economic disparities within the U.S. population. By examining income distribution, employment rates, and poverty levels across different demographic groups, we uncovered significant patterns, including:

- **Income Inequality:** A large portion of the population was concentrated in lower income brackets, suggesting economic inequality.
- **Gender Disparities:** Women faced lower employment rates and higher poverty rates compared to men, indicating gender-based economic challenges.
- **Regional Employment Differences:** Certain regions experienced higher unemployment rates, suggesting geographic labor market disparities.
- **Age and Income Trends:** Income generally increased with age until mid-life, after which it declined due to retirement.

These insights are valuable for guiding future research and informing policy interventions aimed at addressing economic inequality, improving employment opportunities, and supporting vulnerable demographic groups.


