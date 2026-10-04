# Week 3 - Model Optimization

## Project Overview

This project focuses on improving and evaluating machine learning models for the Telco Customer Churn prediction problem.

The main goal of this work was to compare different models, tune their hyperparameters, reduce overfitting, perform customer segmentation, and select a final model using cross-validation before evaluating it once on the test set.

## Dataset

The project uses the Telco Customer Churn dataset.

The target variable is customer churn, where the model predicts whether a customer is likely to leave the service.

## Work Completed

### Part 1: Split Noise

Different random train/validation splits were compared to demonstrate that model performance can vary depending on the random split.

This showed why cross-validation is useful for obtaining more reliable model comparisons.

### Part 2: Cross-Validation

Cross-validation was used to compare Logistic Regression and Random Forest using ROC-AUC.

The models were evaluated using multiple folds rather than relying on a single train/validation split.

### Part 3: Hyperparameter Tuning

Hyperparameter tuning was performed for:

- Logistic Regression
- Random Forest

For Logistic Regression, a validation curve was used to study the effect of `C`.

Grid Search and Random Search were also compared for Random Forest.

### Part 4: XGBoost

XGBoost was trained using early stopping to reduce overfitting.

The validation loss was monitored while increasing the number of boosting trees.

Randomized hyperparameter search was then used to tune the XGBoost model.

### Part 5: K-Means Customer Segmentation

K-Means clustering was used to segment customers based on customer characteristics such as:

- Tenure
- Monthly Charges
- Total Charges
- Number of Services

The elbow method and silhouette score were used to select the number of clusters.

Four customer segments were selected and profiled using churn rate and other customer characteristics.

### Part 6: Principal Component Analysis

Principal Component Analysis (PCA) was used to study the dimensionality and redundancy of the feature space.

The scree plot showed how much variance was explained by each principal component.

PCA was also used to visualize customers in two dimensions and examine the separation between churned and non-churned customers.

### Part 7: Final Model Selection

The final models were compared using cross-validation.

The tuned XGBoost model achieved the highest CV AUC:

**XGBoost CV AUC: 0.8502**

XGBoost was therefore selected as the final model.

The model was then evaluated once on the test set.

**Test AUC: 0.8483**

**Test Recall: 0.521**

**Test Precision: 0.659**

The final trained model was saved as:

```text
churn_model.joblib
