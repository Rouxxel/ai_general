# KNN for Person Purchase Prediction by Ad

## Project Description
This project implements a **Supervised Machine Learning** model using the **K-Nearest Neighbors (KNN)** algorithm. The goal is to predict whether a person will purchase a product based on a set of independent variables such as their gender, age, and estimated salary.

The model learns from historical data where features such as gender, age, and salary are provided, and the target variable is whether or not the person made a purchase (binary classification: "Yes" or "No").

### Problem Type:
- **Supervised Learning**
- **Binary Classification**: Predict whether the person will purchase a product (1) or not (0).

## Dataset
The dataset used in this project contains **400 data points** with the following columns:

- **User ID**: Unique identifier for each user.
- **Gender**: Gender of the user (Male or Female).
- **Age**: Age of the user.
- **EstimatedSalary**: Estimated salary of the user.
- **Purchased**: The target variable, a binary value: 1 for purchased, 0 for not purchased.

Example dataset:
```csv
User ID,Gender,Age,EstimatedSalary,Purchased
15624510,Male,19,19000,0
15810944,Male,35,20000,0
15668575,Female,26,43000,0
15603246,Female,27,57000,0
...
