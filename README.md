# Fraud Detection Machine Learning Model

This repository contains a machine learning model for fraud detection using a dataset that contains fraudulent transactions for a data company. The model is implemented in Jupyter Notebook with Python 3, utilizing libraries such as NumPy and Pandas.

## Contents

1. Data Cleaning
2. Fraud Detection Model Description
3. Variable Selection
4. Key Factors for Predicting Fraudulent Customers
5. Evaluation of Factors
6. Prevention Measures for Infrastructure Updates
7. Determining the Effectiveness of Prevention Actions

## 1. Data Cleaning

The dataset was subjected to data cleaning techniques, which involved addressing missing values, outliers, and multi-collinearity. Missing values in the "Destination transaction of Merchants" were replaced by updating the transaction amount to their new balance destination. Multi-collinearity between attributes was also resolved by discarding the attributes that exhibited strong interdependence.

## 2. Fraud Detection Model Description

The fraud detection model utilized undersampling to tackle the issue of data imbalance. With only 8,213 fraudulent transactions out of 6,362,620 entries, undersampling was employed to balance the data. The majority class was undersampled, resulting in 11,592 samples with an equal distribution of fraudulent and legitimate transactions. A similar undersampling technique was applied to the test data.

Five machine learning models were created: Logistic Regression, K-Nearest Neighbors (KNN), Multinomial Naive Bayes, Decision Tree, and Random Forest. The performance of each model was evaluated using a classification report. Precision and F1 scores were used as the primary evaluation metrics for fraud detection models. The Random Forest Classifier emerged as the best model for the dataset, achieving a precision of 93% and an F1 score of 93%.

## 3. Variable Selection

Variable selection was performed based on the identification of multi-collinearity. Variables with strong interdependence were removed. Additionally, identifier variables such as "nameOrig" and "nameDest" were excluded from the model. All other variables that directly influenced the predictor variable, "isFraud," and exhibited independence from each other were included in the final model.

## 4. Key Factors for Predicting Fraudulent Customers

The key factors that predict fraudulent customers include:

- New accounts receiving funds from unknown sources
- Unverified transactions
- Unusual transactions with large sums

## 5. Evaluation of Factors

These factors make sense in the context of fraud detection. For instance, if a customer has been inactive for an extended period and suddenly engages in unusual transactions involving large sums, it is reasonable to suspect fraudulent activity.

## 6. Prevention Measures for Infrastructure Updates

When updating the company's infrastructure, the following prevention measures should be adopted:

- Implement two-factor authentication and biometric authentication for enhanced security.
- Provide push alerts to customers' mobile phones to enable them to report any fraudulent activity promptly.
- Use secure connections for online transactions.
- Advise customers against downloading unknown or unverified apps that could potentially steal their credentials.
- Educate customers about scam calls and provide knowledge of red flags to watch out for during conversations.

## 7. Determining the Effectiveness of Prevention Actions

The effectiveness of the prevention actions can be determined by:

- Ensuring customers update their banking and transaction apps regularly.
- Encouraging customers to keep their passbooks and statements updated and review them on a weekly basis.
- Raising awareness among customers about common scams and preventive measures to protect themselves from fraud.
