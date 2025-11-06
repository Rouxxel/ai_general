# Customer Segmentation Using Hierarchical Clustering

This project applies an **Unsupervised Machine Learning** technique—**Hierarchical Clustering**—to segment mall customers into distinct groups based on their demographics and spending behavior.

---

## 🎯 Objective

The goal is to group similar customers together using hierarchical clustering so businesses can better understand customer segments and tailor marketing strategies accordingly.

---

## 📦 Dataset

The dataset contains customer demographic and behavioral data from a mall, including gender, age, annual income, and spending score.

### Key Raw Features:
- `CustomerID`: Unique identifier for each customer
- `Gender`: Customer gender (Male/Female)
- `Age`: Age of the customer
- `Annual Income (k$)`: Customer’s annual income in thousands of dollars
- `Spending Score (1-100)`: A score assigned by the mall based on customer spending behavior

---

## 🧮 Features Used for Clustering

After cleaning and preprocessing, the model uses the following features:

- `Gender` (encoded as 0 for Male, 1 for Female)
- `Age`
- Log-transformed `Annual Income (k$)` and `Spending Score (1-100)` to reduce skewness

---

## 🧪 Steps

1. **Data Cleaning & Preprocessing**
   - Encode categorical variables (Gender)
   - Remove extreme outliers based on quantiles
   - Apply log transformations to skewed features (Income, Spending Score)

2. **Feature Scaling**
   - Standardize features using `StandardScaler`

3. **Hierarchical Clustering**
   - Compute linkage matrix using Ward’s method
   - Visualize dendrogram to determine optimal number of clusters

4. **Cluster Assignment**
   - Assign cluster labels using `fcluster` with optimal number of clusters from dendrogram inspection

5. **Evaluation**
   - Profile each cluster with summary statistics (average age, income, spending score, gender distribution)
   - (Optional) Use cluster validity indices suitable for hierarchical clustering

6. **Visualization**
   - Use **PCA** and **t-SNE** for 2D visualization of clusters
   - Visualize dendrogram for cluster hierarchy

7. **Saving Artifacts**
   - Save scaler, linkage matrix, and clustered dataset for future use

---

## 📊 Example Output: Cluster Profiling

Each cluster is analyzed based on average demographics and spending:

| Cluster | Most Common Gender | Avg Age | Avg Income (k$) | Avg Spending Score | Num Customers |
|---------|--------------------|---------|-----------------|--------------------|---------------|
| 1       | Female             | 35.2    | 60.3            | 55.4               | 110           |
| 2       | Male               | 40.7    | 80.1            | 40.7               | 95            |
| 3       | Female             | 29.8    | 40.6            | 80.2               | 130           |

---

## 🧠 Libraries Used

- `pandas`, `numpy`
- `matplotlib`, `seaborn`
- `scipy` (for linkage and dendrogram)
- `scikit-learn` (StandardScaler, PCA, t-SNE)
- `joblib`
- `os`

---

## 🛠 Future Improvements

- Compare with other clustering methods (KMeans, DBSCAN)
- Apply cluster validity metrics specifically designed for hierarchical clustering
- Automate dendrogram threshold selection
