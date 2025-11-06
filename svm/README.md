# Support Vector Machine - Diabetes Detection

A machine learning project implementing Support Vector Machine (SVM) with Linear kernel for early detection of diabetes using health indicators from the BRFSS2015 dataset.

## 🎯 Project Overview

This project applies Support Vector Machine classification to predict diabetes risk based on various health and lifestyle indicators. The model uses Linear SVM with probability calibration and is part of a comparative study of classification algorithms for early diabetes detection.

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

**Linear Support Vector Machine**
- **Kernel**: Linear (for computational efficiency)
- **Implementation**: LinearSVC with CalibratedClassifierCV
- **Key Parameters**:
  - `C=0.01`: Regularization strength (lower = simpler model)
  - `max_iter=2000`: Maximum iterations before convergence warning
  - `class_weight="balanced"`: Handle class imbalance
  - `random_state=42`: Reproducible results

### Why Linear SVM?
- **Computational Efficiency**: Faster training compared to RBF kernel
- **High-Dimensional Data**: Effective for datasets with many features
- **Interpretability**: Linear decision boundary is easier to understand
- **Scalability**: Better performance on large datasets

## 🛠️ Technical Implementation

### Data Preprocessing
- **Missing Value Handling**: SimpleImputer with mean strategy
- **Duplicate Removal**: Automatic detection and removal
- **Class Imbalance**: SMOTE (Synthetic Minority Oversampling Technique)
- **Feature Scaling**: StandardScaler (crucial for SVM performance)

### Model Training
- **Train/Test Split**: 75% training, 25% testing
- **Cross-Validation**: 5-fold stratified cross-validation
- **Probability Calibration**: CalibratedClassifierCV for probability estimates
- **Regularization**: L2 regularization to prevent overfitting

### Evaluation Metrics
- Accuracy Score
- Precision, Recall, F1-Score
- ROC-AUC Score
- Confusion Matrix
- Classification Report
- Cross-validation scores

## 📁 Project Structure

```
svm/
├── dataset/
│   ├── diabetes_binary_health_indicators_BRFSS2015.csv
│   ├── other_considered_datasets/
│   └── download_script_with_links.ipynb
├── logs/
│   └── svm_model.log
├── trained_model/
│   └── [saved model files]
├── svm_model.ipynb
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
cd svm
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

### Usage

1. Open the Jupyter notebook:
```bash
jupyter notebook svm_model.ipynb
```

2. Run all cells to:
   - Load and preprocess the dataset
   - Train the SVM model with calibration
   - Evaluate performance metrics
   - Save the trained model

## 📈 Key Features

- **Linear Decision Boundary**: Efficient and interpretable classification
- **Probability Calibration**: Reliable probability estimates for predictions
- **Robust Preprocessing**: Handles missing values and duplicates
- **Class Imbalance Handling**: SMOTE implementation for balanced training
- **Comprehensive Logging**: Detailed logs for model training process
- **Model Persistence**: Trained model saved for future predictions

## 🔍 Model Performance

The Linear SVM classifier provides:
- **Fast Training**: Linear kernel enables quick model fitting
- **Good Generalization**: Regularization prevents overfitting
- **Probability Estimates**: Calibrated probabilities for risk assessment
- **Scalable Solution**: Efficient for large-scale diabetes screening

## ⚡ Performance Considerations

- **Feature Scaling**: Critical for SVM performance (implemented)
- **Regularization**: C=0.01 provides good bias-variance tradeoff
- **Memory Efficiency**: Linear kernel reduces computational complexity
- **Convergence**: max_iter=2000 ensures model convergence

## 🎓 Academic Context

This implementation is part of a Bachelor Thesis:
**"Application of Machine Learning Techniques for the Early Detection of Diabetes: A Comparative Study of Classification Models"**

Author: Sebastian Russo (ID: 79117092)

## 📝 Technical Notes

- Originally considered RBF kernel but switched to Linear for training efficiency
- CalibratedClassifierCV wraps LinearSVC to provide probability estimates
- SMOTE balances the dataset before training
- Comprehensive logging tracks all preprocessing and training steps
- Model parameters optimized for diabetes detection task

## 🔬 Comparison with Other Models

This SVM implementation can be compared with other models in the portfolio:
- **vs Random Forest**: Faster training, different decision boundary approach
- **vs Logistic Regression**: More complex decision boundary, better for non-linear patterns
- **vs KNN**: More efficient for large datasets, less sensitive to outliers

---

*This project demonstrates the application of Support Vector Machines for healthcare prediction tasks, specifically focusing on early diabetes detection using lifestyle and health indicators with emphasis on computational efficiency and interpretability.*