# Logistic Regression for Titanic Survivors

This project implements a **Supervised Machine Learning Classification** model using **Logistic Regression** to predict the survival of passengers aboard the Titanic based on various independent variables such as class, sex, age, and fare.

---

## Objective

The goal is to build a classification model that predicts whether a given passenger survived (`Survived = 1`) or not (`Survived = 0`) based on relevant features.

---

## Dataset

The dataset contains information about passengers on the Titanic, including demographic and ticket details. The target variable is **Survived**, indicating whether the passenger lived (1) or died (0).

### Sample Data:
| PassengerId | Survived | Pclass | Name                                         | Sex    | Age | SibSp | Parch | Ticket            | Fare    | Cabin | Embarked |
|-------------|----------|--------|----------------------------------------------|--------|-----|--------|--------|--------------------|---------|-------|----------|
| 1           | 0        | 3      | Braund, Mr. Owen Harris                      | male   | 22  | 1      | 0      | A/5 21171          | 7.25    |       | S        |
| 2           | 1        | 1      | Cumings, Mrs. John Bradley (Florence Briggs Thayer) | female | 38  | 1      | 0      | PC 17599           | 71.2833 | C85   | C        |
| 3           | 1        | 3      | Heikkinen, Miss. Laina                       | female | 26  | 0      | 0      | STON/O2. 3101282   | 7.925   |       | S        |
| 4           | 1        | 1      | Futrelle, Mrs. Jacques Heath (Lily May Peel) | female | 35  | 1      | 0      | 113803             | 53.1    | C123  | S        |

---

## Features Used

- `Pclass`: Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd)
- `Sex`: Gender of the passenger
- `Age`: Age of the passenger
- `SibSp`: Number of siblings/spouses aboard
- `Parch`: Number of parents/children aboard
- `Fare`: Fare paid for the ticket
- `Embarked`: Port of Embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)

---

## Steps

1. **Data Preprocessing**
   - Handle missing values (e.g., age, embarked, cabin).
   - Encode categorical variables (`Sex`, `Embarked`) into numeric format.
   - Drop irrelevant columns such as `PassengerId`, `Name`, `Ticket`, and `Cabin`.

2. **Train/Test Split**
   - Split the data into training and testing sets.

3. **Model Training**
   - Use `LogisticRegression` from `scikit-learn` to train the model.

4. **Evaluation**
   - Evaluate the model using accuracy, confusion matrix, and classification report.
