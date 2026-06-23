# Assignment 17.1: Comparing Classifiers

# Overview

The goal of this project was to compare the performance of several classification models in predicting whether a customer would subscribe to a term deposit offered by a Portuguese banking institution. The analysis was conducted using customer demographic and financial information collected during direct marketing campaigns.

# Business Objective

The objective of this analysis was to predict whether a customer would subscribe to a term deposit based on available customer information. By identifying customers who are more likely to subscribe, the bank can improve the effectiveness of its marketing campaigns, reduce unnecessary outreach, and better allocate marketing resources.

# Data Source

The dataset was obtained from the UCI Machine Learning Repository and contains information related to direct marketing campaigns conducted by a Portuguese banking institution. The target variable indicates whether a customer subscribed to a term deposit.

# Data Preparation

The following steps were completed before modeling:

- Selected customer-related features as predictor variables.
- Converted the target variable (y) from categorical values ("yes" and "no") into a binary format (1 and 0).
- Converted to categorical variables using pd.get_dummies().
- Split the data into training and testing datasets using an 80/20 train-test split.

# Models Evaluated

The following classification models were trained and evaluated:

Logistic Regression
K-Nearest Neighbors (KNN)
Decision Tree
Support Vector Machine (SVM)

# Baseline Performance

A baseline model was established by predicting the majority class for all observations. Since most customers did not subscribe to a term deposit, the baseline accuracy was approximately 88.7%.

Model Comparison

Model	Train Accuracy	

Logistic Regression: 88.73%
KNN: 89.07%
Decision Tree: 91.71%
SVM: 88.73%

Test Accuracy

Logistic Regression: 88.74%
KNN: 87.87%
Decision Tree: 86.40%
SVM: 88.74%

# Key Observations

- Logistic Regression and SVM achieved the highest test accuracy at 88.74%.
- KNN produced slightly lower test accuracy but remained competitive.
- The Decision Tree achieved the highest training accuracy but experienced a noticeable drop in test accuracy, potentially due to overfitting.
- SVM required substantially more run time while providing no improvement in accuracy over Logistic Regression.

# Model Improvement

GridSearchCV was used to tune model hyperparameters and compare performance using balanced accuracy.

# Tuned Model Results

Balanced Test Accuracy

Logistic Regression	0.500
KNN	0.536
Decision Tree	0.522
SVM	0.502

# Key Observations
- KNN achieved the highest balanced accuracy after tuning.
- Logistic Regression and SVM performed close to random guessing when evaluated using balanced accuracy.
- The results suggest that customer demographic information alone provides limited predictive power for identifying customers who will subscribe to a term deposit.

# Conclusions

While several classification models were evaluated, none demonstrated strong predictive performance when only customer demographic information was used. Although Logistic Regression and SVM achieved the highest overall accuracy, balanced accuracy revealed that the models struggled to identify the minority class effectively.

The results indicate that additional information would likely improve model performance. This could be economic states, past history, past outcomes.

# Recommendations

- Incorporate additional campaign history and economic variables into future models.
- Continue exploring hyperparameter tuning and feature selection techniques.
- Evaluate alternative performance metrics when working with imbalanced datasets.
- Use predictive modeling to prioritize customer outreach efforts and improve marketing efficiency.

# Notebook

(https://github.com/rahimmerchant07/Assignment_17.1_Comparing_Classifiers/blob/main/Comparing_Classifiers.ipynb)
