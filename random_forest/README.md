# Random Forest - Diabetes Detection

A machine learning project implementing Random Forest Classifier for early detection of diabetes using health indicators from the BRFSS2015 dataset.

## 🎯 Project Overview

This project applies Random Forest classification to predict diabetes risk based on various health and lifestyle indicators. The model is part of a comparative study of classification algorithms for early diabetes detection.

## 📊 Dataset

**Source**: BRFSS2015 (Behavioral Risk Factor Surveillance System 2015)
- **Type**: Binary classification dataset
- **Target**: Diabetes status (0 = No diabetes, 1 = Diabetes)
- **Features**: Health indicators including:
  - BMI (Body Mass Index)
  - Blood pressure status
  - Cholesterol levels
  - Smoking status
  - Physical activity levels
  - Demographic factors (age, gender, income, education)
  - Healthcare access indicators

## 🤖 Algorithm Details

**Random Forest Classifier**
- **Ensemble Method**: Combines multiple decision trees
- **Key Parameters**:
  - `n_estimators=100`: Number of trees in the forest
  - `max_depth=16`: Maximum depth of each tree
  - `max_features="sqrt"`: Features considered for best split
  - `min_samples_split=15`: Minimum samples to split internal node
  - `min_samples_leaf=5`: Minimum samples in leaf node
  - `class_weight="balanced"`: Handle class imbalance

## 🛠️ Technical Implementation

### Data Preprocessing
- **Missing Value Handling**: SimpleImputer with mean strategy
- **Duplicate Removal**: Automatic detection and removal
- **Class Imbalance**: SMOTE (Synthetic Minority Oversampling Technique)
- **Feature Scaling**: StandardScaler for numerical features

### Model Training
- **Train/Test Split**: 75% training, 25% testing
- **Cross-Validation**: Stratified K-Fold validation
- **Hyperparameter Tuning**: Optimized for diabetes detection
- **Parallel Processing**: Utilizes all CPU cores (`n_jobs=-1`)

### Evaluation Metrics
- Accuracy Score
- Precision, Recall, F1-Score
- ROC-AUC Score
- Confusion Matrix
- Classification Report

## 📁 Project Structure

```
random_forest/
├── dataset/
│   ├── diabetes_binary_health_indicators_BRFSS2015.csv
│   ├── other_considered_datasets/
│   └── download_script_with_links.ipynb
├── logs/
│   └── random_forest_model.log
├── trained_model/
│   └── [saved model files]
├── random_forest_model.ipynb
├── requirements.txt
└── README.md
```

## 🚀 Getting Started

### Prerequisites
- Python 3.7+
- Required packages (see requirements.txt)

### Installation

1. Navigate to the project directory:
```bash
cd random_forest
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

### Usage

1. Open the Jupyter notebook:
```bash
jupyter notebook random_forest_model.ipynb
```

2. Run all cells to:
   - Load and preprocess the dataset
   - Train the Random Forest model
   - Evaluate performance metrics
   - Save the trained model

## 📈 Key Features

- **Robust Preprocessing**: Handles missing values and duplicates
- **Class Imbalance Handling**: SMOTE implementation for balanced training
- **Comprehensive Logging**: Detailed logs for model training process
- **Model Persistence**: Trained model saved for future predictions
- **Performance Visualization**: Confusion matrix and metric plots

## 🔍 Model Performance

The Random Forest classifier provides:
- High interpretability through feature importance analysis
- Robust performance on imbalanced datasets
- Resistance to overfitting through ensemble approach
- Efficient training with parallel processing

## 🎓 Academic Context

This implementation is part of a Bachelor Thesis:
**"Application of Machine Learning Techniques for the Early Detection of Diabetes: A Comparative Study of Classification Models"**

Author: Sebastian Russo (ID: 79117092)

## 📝 Notes

- The model uses balanced class weights to handle dataset imbalance
- SMOTE is applied to generate synthetic samples for minority class
- Comprehensive logging tracks all preprocessing and training steps
- Model parameters are optimized for diabetes detection task

---

*This project demonstrates the application of ensemble methods for healthcare prediction tasks, specifically focusing on early diabetes detection using lifestyle and health indicators.*