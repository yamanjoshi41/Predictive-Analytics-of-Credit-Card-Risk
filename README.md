# Predictive-Analytics-of-Credit-Card-Risk

This is the detailed report showing the credit card risk assessment uisng differnt machine learning models. This was conducted using Rapidminer software. 

# Predictive Analytics for Credit Risk Assessment

This project focuses on predictive analytics for assessing credit risk in loan applicants. The goal is to build a model that classifies loan applicants into "Good" or "Bad" credit standing based on various attributes such as credit history, savings, account balance, and employment status. This was conducted using Rapidminer software and Python.

## Table of Contents
- [Business Overview](#business-overview)
- [Data Analysis](#data-analysis)
- [Data Preprocessing](#data-preprocessing)
- [Model Evaluation](#model-evaluation)
  - [Decision Tree](#decision-tree)
  - [Naïve Bayes](#naïve-bayes)
  - [Random Forest](#random-forest)
  - [KNN](#knn)
  - [Logistic Regression](#logistic-regression)
  - [GLM](#glm)
  - [Neural Network](#neural-network)
  - [SVM](#svm)
- [Final Model Selection](#final-model-selection)
- [Ensemble Model](#ensemble-model)
- [License](#license)

## Business Overview
The dataset contains 425 records of loan applicants, each with 15 variables, including credit history, checking account status, gender, and personal status. The target variable is "Credit Standing," a binary classification problem (Good/Bad). The objective is to predict the credit standing of loan applicants using supervised learning techniques.

## Data Analysis
The dataset includes both categorical and numerical variables. The target variable is "Credit Standing," and the independent variables include:
- Credit History
- Checking Account Balance
- Savings Account Balance
- Employment Status
- Personal Information (Age, Gender, etc.)

## Data Preprocessing
- **Variable Renaming**: Variables were renamed for better understanding (e.g., "Age Subtracted 1 from Original Age Variable" was renamed to "Age").
- **Missing Values**: The "Gender" variable was excluded due to missing values and potential bias.
- **Normalization**: Variables like "Months Acct" and "Residence Time" were normalized using z-score.

## Model Evaluation
Several models were evaluated for their performance in predicting credit standing:

### Decision Tree
- **Accuracy**: 63.64%
- **Precision**: 61.54% (Good), 66.67% (Bad)
- **Recall**: 72.73% (Good), 54.55% (Bad)

### Naïve Bayes
- **Accuracy**: 50.0%
- **Precision**: 66.67% (Good), 70.00% (Bad)
- **Recall**: 72.73% (Good), 63.64% (Bad)

### Random Forest
- **Accuracy**: 68.18%
- **Precision**: 71.14% (Good), 70.30% (Bad)
- **Recall**: 70.44% (Good), 71.00% (Bad)

### KNN
- **Accuracy**: 45.45%
- **Precision**: 62.50% (Good), 57.14% (Bad)
- **Recall**: 45.45% (Good), 72.73% (Bad)

### Logistic Regression
- **Accuracy**: 68.18%
- **Precision**: 70.22% (Good), 68.18% (Bad)
- **Recall**: 70.22% (Good), 68.18% (Bad)

### GLM
- **Accuracy**: 63.64%
- **Precision**: 70.47% (Good), 63.64% (Bad)
- **Recall**: 70.47% (Good), 63.64% (Bad)

### Neural Network
- **Accuracy**: 63.64%
- **Precision**: 62.28% (Good), 63.64% (Bad)
- **Recall**: 62.28% (Good), 63.64% (Bad)

### SVM
- **Accuracy**: 59.09%
- **Precision**: 69.98% (Good), 59.09% (Bad)
- **Recall**: 69.98% (Good), 59.09% (Bad)

## Final Model Selection
The final model was selected based on the following criteria:
1. **Performance on Test Data**: Models with higher accuracy on the test set were preferred.
2. **Overfitting**: Models with a small difference between training and test accuracy were chosen.
3. **Model Complexity**: Simpler models like Logistic Regression were preferred for interpretability.

| Model               | Training Accuracy | Test Accuracy | Difference |
|---------------------|-------------------|---------------|------------|
| Logistic Regression | 70.22%            | 68.18%        | 2.04%      |
| Neural Network      | 62.28%            | 63.64%        | -1.36%     |

**Final Choice**: Logistic Regression was selected due to its balance of accuracy, simplicity, and interpretability.

## Ensemble Model
An ensemble model was also explored using a voting mechanism to combine the predictions of multiple models. The ensemble model showed improved performance, but Logistic Regression remained the preferred choice due to its simplicity.


