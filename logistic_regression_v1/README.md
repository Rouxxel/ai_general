# Logistic Regression for Breast Cancer Classification

This project implements a **Supervised Machine Learning Classification** model using **Logistic Regression** to predict whether a patient has breast cancer or not based on various features from a breast cancer dataset. 

### Objective:
The goal of this model is to classify a patient as either **malignant** or **benign** based on independent variables such as the size of the tumor, its smoothness, compactness, and various other measurements.

### Dataset:
The dataset contains information about various features extracted from breast cancer biopsies, and the target variable is the **diagnosis** (either "M" for malignant or "B" for benign). 

#### Sample Data:
| id      | diagnosis | radius_mean | texture_mean | perimeter_mean | area_mean | smoothness_mean | compactness_mean | concavity_mean | concave points_mean | symmetry_mean | fractal_dimension_mean | radius_se | texture_se | perimeter_se | area_se | smoothness_se | compactness_se | concavity_se | concave points_se | symmetry_se | fractal_dimension_se | radius_worst | texture_worst | perimeter_worst | area_worst | smoothness_worst | compactness_worst | concavity_worst | concave points_worst | symmetry_worst | fractal_dimension_worst |
|---------|-----------|-------------|--------------|----------------|-----------|-----------------|------------------|-----------------|----------------------|----------------|------------------------|-----------|------------|--------------|---------|----------------|----------------|--------------|------------------|--------------|----------------------|--------------|----------------|-----------------|-----------|------------------|-------------------|----------------|---------------------|------------------|
| 842302  | M         | 17.99       | 10.38        | 122.8          | 1001      | 0.1184          | 0.2776           | 0.3001          | 0.1471               | 0.2419         | 0.07871                | 1.095     | 0.9053     | 8.589        | 153.4   | 0.006399        | 0.04904        | 0.05373      | 0.01587           | 0.03003      | 0.006193               | 25.38        | 17.33         | 184.6           | 2019      | 0.1622           | 0.6656            | 0.7119          | 0.2654               | 0.4601         | 0.1189               |
| 842517  | M         | 20.57       | 17.77        | 132.9          | 1326      | 0.08474         | 0.07864          | 0.0869          | 0.07017              | 0.1812         | 0.05667                | 0.5435    | 0.7339     | 3.398        | 74.08   | 0.005225        | 0.01308        | 0.0186       | 0.0134            | 0.01389      | 0.003532               | 24.99        | 23.41         | 158.8           | 1956      | 0.1238           | 0.1866            | 0.2416          | 0.186              | 0.275          | 0.08902              |

The dataset includes the following columns:
- **radius_mean**: Mean of distances from the center to points on the perimeter.
- **texture_mean**: Standard deviation of gray-scale values.
- **perimeter_mean**: Mean size of the tumor's perimeter.
- **area_mean**: Mean area of the tumor.
- **smoothness_mean**: Mean of local variations in radius lengths.
- **compactness_mean**: Mean of perimeter^2 / area - 1.0.
- **concavity_mean**: Mean of severity of concave portions of the contour.
- **symmetry_mean**: Mean of symmetry.
- **fractal_dimension_mean**: Mean of the "coastline approximation" of the tumor.

And other measurements related to tumor properties.

### Steps in the Model:
1. **Data Preprocessing**:
    - Load the dataset.
    - Clean and prepare data.
    - Split the data into features (X) and target (Y).

2. **Model Implementation**:
    - Train a Logistic Regression model using the training data.
    - Evaluate the model using test data.
    - Calculate accuracy, precision, recall, F1-score, and other relevant metrics.
    
3. **Visualization**:
    - Confusion matrix to evaluate the classification performance.
    - Data visualizations such as correlation matrices and ROC curves.

### Libraries Used:
- **pandas**: Data manipulation and analysis.
- **numpy**: Numerical operations.
- **matplotlib**: Visualization of data.
- **seaborn**: Visualization for data exploration.
- **scikit-learn**: Machine learning model implementation and evaluation (Logistic Regression, accuracy metrics, train/test split).
