# Bank Marketing Prediction using Machine Learning

## Project Overview

This project builds a Machine Learning model to predict whether a customer will subscribe to a bank term deposit or not.

The model is trained using the Bank Marketing dataset. Different customer information such as age, job, education, balance, housing loan, contact type, previous campaign history, etc. are used to predict customer subscription behavior.

The main goal of this project is to help banks identify potential customers who are more likely to subscribe to their services.

---

## Dataset

Dataset Used:

Bank Marketing Dataset

Dataset Size:
- Total Samples: 45,211
- Total Features: 16
- Target Variable: `y`

Target Classes:

- 0 → Customer did not subscribe
- 1 → Customer subscribed

---

## Machine Learning Approach

The following steps were performed:

1. Data Loading
2. Exploratory Data Analysis
3. Data Preprocessing
4. Feature Encoding
5. Train-Test Split
6. Handling Class Imbalance using SMOTE
7. Model Training
8. Model Evaluation
9. Threshold Optimization
10. Model Saving

---

## Model Used

### XGBoost Classifier

XGBoost was selected because it provides:

- High prediction accuracy
- Better handling of complex patterns
- Good performance on structured/tabular data
- Feature importance analysis

---

## Data Preprocessing

The preprocessing pipeline includes:

### Numerical Features:
- Standard Scaling

### Categorical Features:
- One Hot Encoding

### Class Imbalance:
SMOTE technique was applied to balance the minority class.

Before SMOTE:
## Model Architecture

The proposed model uses **XGBoost Classifier** for predicting whether a customer will subscribe to a bank term deposit.

Architecture Flow:


Input Customer Data
|
↓
Data Preprocessing Pipeline
|
↓
Numerical Features
(Standard Scaling)
|
↓
Categorical Features
(One Hot Encoding)
|
↓
SMOTE
(Class Balancing)
|
↓
XGBoost Classifier
(Gradient Boosting Decision Trees)
|
↓
Probability Prediction
|
↓
Threshold Optimization
(Threshold = 0.35)
|
↓
Final Classification
YES / NO


### Model Components:

- **Preprocessing Pipeline:** Converts raw customer information into machine learning compatible format.
- **Standard Scaling:** Normalizes numerical features for better model performance.
- **One Hot Encoding:** Converts categorical variables into numerical representations.
- **SMOTE:** Handles class imbalance by generating synthetic samples for the minority class.
- **XGBoost Classifier:** Learns complex patterns from customer data and performs prediction.
- **Threshold Optimization:** Adjusts the decision boundary to improve detection of potential customers.

The final model predicts whether a customer is likely to subscribe to a bank term deposit.