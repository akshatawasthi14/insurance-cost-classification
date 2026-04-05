Insurance Cost Analysis and Classification
Overview

This project applies data analysis, preprocessing, feature engineering, and machine learning techniques to an insurance dataset to understand the factors influencing medical charges and to predict whether an individual is likely to incur high or low insurance costs.

The workflow follows a structured machine learning pipeline, starting with exploratory data analysis and statistical feature analysis, and culminating in a classification model built using Logistic Regression.

Problem Statement

Medical insurance charges vary significantly based on individual characteristics such as age, lifestyle, and health indicators. The objective of this project is to:

Analyze and identify key factors affecting insurance charges
Use statistical methods to evaluate feature importance
Transform the problem into a classification task (high vs low charges)
Build a machine learning model to predict insurance cost categories
Dataset Description

The dataset contains demographic and health-related information about individuals along with their insurance charges.

Features:

age: Age of the individual
sex: Gender
bmi: Body Mass Index
children: Number of dependents
smoker: Smoking status
region: Residential region

Target:

charges: Continuous insurance cost
high_charges: Binary variable created using the median of charges (0 = low, 1 = high)
Methodology
Exploratory Data Analysis

Initial analysis was performed to understand the dataset structure, distributions, and relationships between variables. This included checking data types, summary statistics, missing values, and duplicates.

Data Cleaning
Duplicate records were removed
Data types were verified and corrected
Categorical variables such as sex and smoker were converted into numerical format
Feature Engineering
One-hot encoding was applied to the region feature
A binary gender feature (is_female) was created
A new target variable high_charges was created by splitting charges based on the median
Feature Analysis

Statistical methods were used to evaluate relationships between features and insurance charges:

Pearson correlation was used to measure linear relationships
Chi-square tests were used to assess dependency between categorical variables and the target

Key insights:

Smoking status is the strongest predictor of high insurance charges
BMI and age show moderate positive relationships with charges
Gender, region, and number of children have minimal impact

These findings guided feature selection for the model.

Model Building

A Logistic Regression classification model was built to predict whether an individual falls into the high or low insurance cost category.

Steps:

Selected relevant features (age, bmi, smoker, children, gender)
Split the dataset into training and testing sets
Applied feature scaling using StandardScaler (after splitting to avoid data leakage)
Trained the model on the training data
Model Evaluation

The model was evaluated using standard classification metrics:

Accuracy
Precision
Recall
F1-score
Confusion matrix

The model achieved approximately 90% accuracy with balanced precision and recall, indicating strong and reliable performance across both classes.

Results and Interpretation

The model successfully captures patterns in the data and is able to distinguish between high and low insurance cost individuals. The results align with the feature analysis, confirming that smoking, BMI, and age are key drivers of insurance charges.

Conclusion

This project demonstrates the importance of combining data analysis and machine learning to solve real-world problems. By using statistical techniques for feature understanding and applying a classification model, the project effectively predicts insurance cost categories and highlights the impact of major contributing factors.

Technologies Used

Python
Pandas, NumPy
Matplotlib, Seaborn
Scikit-learn
SciPy

Learning Outcomes

Understanding of end-to-end machine learning workflow
Practical experience with data cleaning and preprocessing
Application of feature engineering techniques
Use of statistical methods for feature analysis
Building and evaluating classification models
