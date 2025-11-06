# Linear Regression for 1000 Companies

## Overview
This project implements a **Supervised Machine Learning** model that predicts the **Profit** of a company based on four independent variables using **Linear Regression**. The goal is to model the relationship between various company expenditures and the profit, using the available data to train a regression model and predict the profit for future companies.

## Dataset

The dataset consists of the following columns:

1. **R&D Spend**: The amount of money spent on research and development.
2. **Administration**: The amount of money spent on administrative expenses.
3. **Marketing Spend**: The amount of money spent on marketing.
4. **State**: The location of the company (categorical variable with values such as New York, California, and Florida).
5. **Profit**: The profit of the company (dependent variable that the model is trying to predict).

### Sample Data

| R&D Spend  | Administration | Marketing Spend | State      | Profit   |
|------------|----------------|-----------------|------------|----------|
| 165349.2   | 136897.8       | 471784.1        | New York   | 192261.83|
| 162597.7   | 151377.59      | 443898.53       | California | 191792.06|
| 153441.51  | 101145.55      | 407934.54       | Florida    | 191050.39|
| 144372.41  | 118671.85      | 383199.62       | New York   | 182901.99|
| 142107.34  | 91391.77       | 366168.42       | Florida    | 166187.94|
| 131876.9   | 99814.71       | 362861.36       | New York   | 156991.12|
| 134615.46  | 147198.87      | 127716.82       | California | 156122.51|

This dataset consists of **1000 companies** with their corresponding features and profit values.

## Objective

The objective of this project is to use **Linear Regression** to predict the **Profit** of a company given the following inputs:

- R&D Spend
- Administration
- Marketing Spend
- State

## Steps Involved:

1. **Data Preprocessing:**
   - Separate dependent and independent variables.
   - Handle categorical variables (e.g., "State") using encoding techniques.
   - Split data into training and testing sets.

2. **Modeling:**
   - Train a **Linear Regression** model using the training data.
   - Test the model on unseen data (testing set).

3. **Evaluation:**
   - Evaluate model performance using metrics such as **Mean Squared Error (MSE)** and **R-squared**.
   - Visualize the results.

4. **Prediction:**
   - Use the trained model to make predictions for new data points.
