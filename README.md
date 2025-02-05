# Loan Default Prediction Based on the German Credit Data

This repository contains an analysis and implementation of a Loan Default Prediction model using the German Credit Data. The primary objective of this project is to predict whether a loan applicant is likely to default on his/her loan. The model was built using logistic regression with L1 regularization (Lasso) to enhance interpretability and handle feature selection.

## Table of Contents

1. Introduction
2. Dataset
3. Methodology
4. Results

## 1. Introduction

Loan default prediction is a critical task for financial institutions to minimize risk and make informed lending decisions. This project utilizes logistic regression with L1 regularization to identify significant predictors of loan default and improve model interpretability by shrinking irrelevant features to zero.

The project demonstrates the entire pipeline, from data preprocessing to model evaluation, and provides insights into the importance of different features.

## 2. Dataset

The dataset used is the German Credit Data, which contains information about loan applicants and their corresponding loan statuses (good/bad credit). The features include demographic information, financial details, and loan-specific attributes.

* Dataset source: https://openml.org/search?type=data&sort=runs&status=active&id=31
* Target variable: class (Good Credit = 0, Bad Credit = 1)
* Number of samples: 1,000
* Features: 20 (checking_status, duration, credit_history, purpose, credit_amount, savings_status, employment, installment_commitment, personal_status, other_parties, residence_since, property_magnitude, age, other_payment_plans, housing, existing_credits, job, num_dependents, own_telephone, foreign_worker)
* Number of missing values: 0

## 3. Methodology

1. Data Preprocessing:

  * Data exploration.
  * Categorical variable encoding using One-Hot Encoding.
  * Standardization of numerical features to improve model performance.

2. Model Development:

  * Logistic regression with L1 regularization (Lasso) was used to:
    * Predict loan default probability.
    * Perform feature selection by shrinking irrelevant feature coefficients to zero.

3. Model Evaluation:

  * Metrics used:
    * Accuracy: overall model performance.
    * Precision, Recall, F1-Score: To measure performance on predicting loan defaults.
    * ROC-AUC: To evaluate the model's discriminative power.
  * 10-fold cross-validation was applied to ensure robust evaluation.
  
## 4. Results

  * Feature Selection:
    * L1 Regularization automatically selected the most predictive features, reducing redundancy and improving interpretability.
    * Key predictors include:
      * Checking account status
      * Loan duration
      * Credit history 
      * Employment status
      * Loan purpose

  * Model Performance:
      * Accuracy: ~76.1%
      * F1-Score for Default (Class 1): ~0.66
      * ROC-AUC: ~0.77
