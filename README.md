📘 Simple Project Documentation – E-Commerce Furniture Prediction
1. Project Overview

This project predicts:

Final selling price of furniture

Whether the item will sell or not

Price tag category (Budget, Premium, etc.)

The project uses:

Python

Machine Learning

Excel Dashboard

SQL for data analysis

2. Dataset

The dataset contains:

Category

Material

Condition

Seller rating

Demand score

Base price

Discount

Final price (Target)

Loaded using:

df = pd.read_csv("furniture_data.csv")

3. Steps in the Project
a. Data Preprocessing

Handling missing values

Label encoding categorical columns

Removing outliers

Feature scaling

Splitting data into train & test

b. Exploratory Data Analysis (EDA)

Price distribution

Category-wise average prices

Discount vs final price

Correlation heatmap

c. Feature Engineering

Selecting important features

Creating new features (price difference, demand score groups)

4. Machine Learning Models

Used:

Random Forest Regressor → Predict final price

Random Forest Classifier → Predict price tag

Random Forest Classifier → Predict “Will it sell?”

Model gives:

Predicted Price: 30,704.70
Sell? : Yes
Tag : Budget Friendly

5. SQL Queries

Stored in furniture_queries.sql.

Examples:

SELECT * FROM furniture_data
ORDER BY final_price DESC LIMIT 5;

SELECT category, AVG(final_price)
FROM furniture_data
GROUP BY category;

6. Excel Dashboard

The dashboard shows:

Total sales

Average price per category

Highest selling price

Category-wise bar chart

KPI cards

8. Conclusion

This is a complete end-to-end ML project covering:

Data cleaning

EDA

Model training & evaluation

SQL analysis

Excel visualization
