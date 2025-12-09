# E-Commerce Furniture Prediction – Documentation
## 1. Project Overview
This project predicts the final selling price of furniture,
whether the item will sell, and its price tag category using machine learning.
## 2. Dataset
The dataset includes:
- Category
- Material
- Condition
- Seller rating
- Demand score
- Base price
- Discount
- Final price (Target)
## 3. Steps in the Project
### a. Data Preprocessing
- Handle missing values
- Encode categorical data
- Remove outliers
- Scale features
- Train-test split
### b. Exploratory Data Analysis
- Price distribution
- Category-wise average price
- Discount vs final price
- Correlation heatmap
### c. Feature Engineering
- Selecting important features
- Creating new attributes
## 4. Machine Learning Models
Models used:
- Random Forest Regressor
- Random Forest Classifier
Output includes:
- Predicted price
- Will it sell?
- Predicted tag
## 5. SQL Queries
Included queries:
- Create table
- Fetch highest-priced items
- Average price by category
- Demand-based filtering
## 6. Excel Dashboard
Dashboard shows:
- KPIs (total sales, avg price)
- Category-wise charts
- Material distribution
## 7. Conclusion
This project provides a full ML workflow with SQL + Dashboard support


SELECT item_id, base_price, discount,
(base_price - (base_price * (discount/100))) AS expected_price
FROM furniture_data;


2.# Project Documentation: Analysis Notebook Summary
## Introduction
This document summarizes the workflow and results from the uploaded Jupyter Notebook. It includes data loading, cleaning, exploratory data analysis (EDA), modeling, and evaluation steps.
## Dataset
The notebook loads the dataset, inspects basic information, handles missing values, and performs preprocessing appropriate for the model.
## Exploratory Data Analysis EDA steps include:
-	Viewing distributions of numerical features
-	Analyzing correlations
-	Visualizing patterns and trends
## Data Preprocessing
Common steps include:
-	Handling null values
-	Encoding categorical variables
-	Scaling numerical fields (if used)
-	Splitting the dataset into training and testing subsets
## Modeling
Machine learning models are trained using:
-	Train-test split
-	Model training (e.g., RandomForest, Logistic Regression, etc.)
-	Hyperparameter tuning (if present)
## Evaluation
The notebook evaluates predictions using:
-	Accuracy score
-	Confusion matrix
-	Visual plots
## Conclusion
The notebook successfully demonstrates the end-to-end ML workflow. You can enrich this documentation further with domain-specific explanations, screenshots, and final observations.


