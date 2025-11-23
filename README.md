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

##SQL QUeries##
CREATE TABLE furniture_data (
    item_id INT PRIMARY KEY,
    category VARCHAR(50),
    material VARCHAR(50),
    base_price FLOAT,
    discount FLOAT,
    final_price FLOAT,
    seller_rating FLOAT,
    demand_score INT
);

INSERT INTO furniture_data VALUES
(1,'Chair','Wood',3000,10,2700,4.5,80);

SELECT * FROM furniture_data
ORDER BY final_price DESC
LIMIT 5;

SELECT category, AVG(final_price)
FROM furniture_data
GROUP BY category;

SELECT * FROM furniture_data
WHERE demand_score >= 80;

SELECT discount, AVG(final_price)
FROM furniture_data
GROUP BY discount;

SELECT item_id, base_price, discount,
(base_price - (base_price * (discount/100))) AS expected_price
FROM furniture_data;
  
