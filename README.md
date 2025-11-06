# Machine Learning Portfolio

A comprehensive collection of machine learning projects implementing various algorithms and techniques for classification, regression, and clustering tasks. This repository consolidates multiple ML models that were previously maintained in separate repositories.

## 🎯 Overview

This portfolio demonstrates practical implementations of fundamental machine learning algorithms across different domains including healthcare, business analytics, customer segmentation, and predictive modeling.

## 📊 Projects

### Supervised Learning

#### Classification Models

**🌺 [Decision Tree - Iris Flower Classification](./decision_tree/)**
- **Algorithm**: Decision Tree Classifier
- **Dataset**: Classic Iris dataset (150 samples, 3 species)
- **Task**: Multi-class classification of iris species based on sepal/petal measurements
- **Features**: Sepal length/width, petal length/width

**🏥 [Logistic Regression - Breast Cancer Detection](./logistic_regression_v1/)**
- **Algorithm**: Logistic Regression
- **Dataset**: Breast cancer diagnostic data
- **Task**: Binary classification (malignant vs benign)
- **Features**: Tumor characteristics (radius, texture, perimeter, area, smoothness, etc.)

**🚢 [Logistic Regression - Titanic Survival Prediction](./logistic_regression_v2/)**
- **Algorithm**: Logistic Regression
- **Dataset**: Titanic passenger data
- **Task**: Binary classification (survived vs not survived)
- **Features**: Passenger class, sex, age, fare, embarkation port

**🛒 [K-Nearest Neighbors - Purchase Prediction](./knn/)**
- **Algorithm**: K-Nearest Neighbors (KNN)
- **Dataset**: Customer demographic and purchase data (400 samples)
- **Task**: Binary classification (will purchase vs won't purchase)
- **Features**: Gender, age, estimated salary

#### Regression Models

**💼 [Linear Regression - Company Profit Prediction](./linear_regression/)**
- **Algorithm**: Linear Regression
- **Dataset**: 1000 companies with expenditure data
- **Task**: Predict company profit
- **Features**: R&D spend, administration costs, marketing spend, state location

### Unsupervised Learning

#### Clustering Models

**🛍️ [K-Means Clustering - Customer Segmentation](./k_means_cluster/)**
- **Algorithm**: K-Means Clustering
- **Dataset**: E-commerce customer transaction data
- **Task**: Customer segmentation based on purchasing behavior
- **Features**: Number of purchases, total quantity, total amount spent
- **Evaluation**: Elbow method, silhouette analysis, multiple cluster validity metrics

**👥 [Hierarchical Clustering - Mall Customer Segmentation](./hierarchical_clustering/)**
- **Algorithm**: Hierarchical Clustering (Ward's method)
- **Dataset**: Mall customer demographic and spending data
- **Task**: Customer segmentation for targeted marketing
- **Features**: Gender, age, annual income, spending score
- **Visualization**: Dendrogram analysis, PCA, t-SNE

## 🛠️ Technologies & Libraries

- **Python 3.x**
- **Core ML Libraries**: scikit-learn, pandas, numpy
- **Visualization**: matplotlib, seaborn
- **Data Processing**: scipy, joblib
- **Dimensionality Reduction**: PCA, t-SNE
- **Model Persistence**: joblib

## 📁 Repository Structure

Each project is self-contained with its own directory including:
- Detailed README with project description and methodology
- Jupyter notebooks or Python scripts
- Requirements file for dependencies
- Trained models and preprocessing artifacts
- Data visualizations and analysis results

## 🚀 Getting Started

1. Clone the repository:
```bash
git clone <repository-url>
cd ai_general
```

2. Install dependencies for all projects:
```bash
pip install -r all_reqs.txt
```

3. Navigate to any specific project directory and follow its individual README for detailed instructions.

## 📈 Key Learning Outcomes

- **Supervised Learning**: Classification and regression techniques
- **Unsupervised Learning**: Clustering and customer segmentation
- **Data Preprocessing**: Feature engineering, scaling, encoding
- **Model Evaluation**: Various metrics and validation techniques
- **Visualization**: Data exploration and results presentation
- **Real-world Applications**: Healthcare, business, e-commerce domains

## 🔄 Future Enhancements

- Deep learning implementations
- Ensemble methods and model stacking
- Time series analysis projects
- Natural language processing applications
- Computer vision projects
- MLOps and model deployment examples

---

*This repository serves as a practical demonstration of machine learning fundamentals and their applications across various domains.*
