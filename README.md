# credit_card_fraud_detection
Credit Card Fraud Detection Using ML

# Credit Card Fraud Detection using Machine Learning

## Overview
This project aims to detect fraudulent transactions in a credit card dataset using machine learning techniques. The dataset consists of transactions labeled as fraudulent or legitimate.

## Dataset
Dataset Link : https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud
The dataset contains 284,807 rows with the following columns:

- `Time`: The time elapsed between this transaction and the first transaction in the dataset.
- `V1` to `V28`: Principal Component Analysis (PCA) applied features.
- `Amount`: The transaction amount.
- `Class`: The class label (1 for fraudulent, 0 for legitimate).

## Data Preprocessing
1. **Basic Analysis**: 
   - Checked for null values, dataset shape, and descriptive statistics using `df.info()` and `df.describe()`.
2. **Data Visualization**: 
   - Used heatmaps to study relationships between columns and calculate correlation values for the `Class` column.

## Handling Class Imbalance
The dataset was highly imbalanced:
- Class 0 (Legitimate transactions): 284,315
- Class 1 (Fraudulent transactions): 492

To address this, I performed undersampling:
- Sampled 492 rows with class 0 (legitimate transactions).
- Combined with 492 rows of class 1 (fraudulent transactions).

## Model Training
Performed train-test split and stratified on the `Class` column to ensure balanced training and testing sets. Trained two models for comparison:
1. **Logistic Regression** (before and after sampling)

## Model Evaluation
Evaluated models using:
- **Accuracy Score**
- **Confusion Matrix**
- **Classification Report**
- **ROC AUC Score**
- **Precision-Recall Curve**
- **AUC (Area Under Curve)**

### Results
- **Without Sampling**: AUC (recall, precision) = 0.6181
- **With Sampling**: AUC (recall, precision) = 0.9568

The AUC value is crucial as it considers both recall (sensitivity) and precision, providing a balanced measure of the model's performance, especially important for imbalanced datasets.

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/riitk/credit_card_fraud_detection.git
   cd credit-card-fraud-detection
