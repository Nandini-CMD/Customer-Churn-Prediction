# 📉 Customer Churn Prediction Using Machine Learning

Welcome to the **Customer Churn Prediction** project! This project uses machine learning to analyze customer behavior and predict whether a customer is likely to leave (churn) from a banking service. Designed using real-world data, this pipeline brings together data science, EDA, and predictive modeling into a single, interactive notebook.

---

## 🧠 What is Customer Churn?

Customer churn refers to the loss of clients or subscribers. It’s a critical metric for businesses because acquiring a new customer can cost **5x more** than retaining an existing one. By predicting churn in advance, companies can implement retention strategies and improve customer satisfaction.

---

## 📂 Dataset Description

This project uses the `Churn_Modelling.csv` dataset, which contains **10,000 customer records** from a bank.

### 🔍 Key Columns:

| Column            | Description                                    |
|-------------------|------------------------------------------------|
| `CustomerId`      | Unique ID of the customer                      |
| `Surname`         | Customer’s last name                           |
| `CreditScore`     | Credit score (affects churn probability)       |
| `Geography`       | Country (France, Germany, Spain)               |
| `Gender`          | Male/Female                                    |
| `Age`             | Age of the customer                            |
| `Tenure`          | Years the customer stayed with the bank        |
| `Balance`         | Current account balance                        |
| `NumOfProducts`   | Number of bank products used                   |
| `HasCrCard`       | Whether they have a credit card (1/0)          |
| `IsActiveMember`  | Activity status (active or not)                |
| `EstimatedSalary` | Yearly estimated salary                        |
| `Exited`          | Target variable: 1 if customer left, 0 if not  |

---

## 🔧 Project Workflow

This project follows a structured pipeline from raw data to actionable insights.

### 📊 1. Exploratory Data Analysis (EDA)
- Distribution of churned vs. retained customers
- Effect of age, geography, and activity on churn
- Correlation matrix to understand feature relationships
- Class imbalance check

### 🧹 2. Data Preprocessing
- Encoding categorical features (OneHot & Label Encoding)
- Feature scaling using `StandardScaler`
- Splitting into training and test sets

### 🧠 3. Model Training & Evaluation
Trained multiple models for comparison:
- Logistic Regression
- Random Forest Classifier
- **XGBoost Classifier** ✅ (Best Performing)

Evaluated using:
- Accuracy
- Confusion Matrix
- ROC-AUC Curve
- Precision, Recall, F1-score

### 🔍 4. Feature Importance
From XGBoost:
- `IsActiveMember`, `Age`, and `CreditScore` were top predictors of churn.

---

## 📈 Model Performance

| Model               | Accuracy | ROC-AUC | Notes                           |
|---------------------|----------|---------|---------------------------------|
| Logistic Regression | ~80%     | Moderate| Fast, interpretable             |
| Random Forest       | ~84%     | High    | Handles non-linearity well      |
| XGBoost             | ~86%     | High    | Best overall performance ✅      |

---

## 📸 Suggested Visuals (Add Screenshots to `images/` folder)

You can add visuals like these to enhance the project:

- 📊 Churn Distribution → `images/churn_distribution.png`
- 🔥 Feature Importance → `images/feature_importance.png`
- 🌍 Churn by Geography → `images/geography_churn.png`
- 📈 ROC Curve Comparison → `images/roc_curve.png`


![Churn Distribution](images/churn_distribution.png)
![Feature Importance](images/feature_importance.png)
