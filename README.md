# Module 12 Report

## Overview of the Analysis

### Purpose: ###

The purpose of this analysis was to train and evaluate a machine learning model based on loan risk. A dataset was provided that contained historical lending activity from a Peer-To-Peer lending services company. The ideal outcome of this model is to identify the creditworthiness of borrowers. The model will be used to predict whether a loan from the company will be high risk or low risk. The model will be evaluated on the accuracy of its predictions.

### Financial Information Provided in the Dataset: ###

- loan_size	
- interest_rate
- borrower_income
- debt_to_income
- num_of_account
- derogatory_marks
- total_debt
- loan_status

### Stages of the Machine Learning Process: ###

1. Read the CSV file into a Pandas DataFrame
1. Import the train_test_learn module from sklearn and split the data using train_test_split
1. Import the LogisticRegression module from sk-learn, instantiate the Logistic Regression model, and fit the model using training data 
1. Make a prediction using the testing data
1. Print the balanced_accuracy score of the model
1. Generate a confusion matrix for the model
1. Print the classification report for the model
1. Import the RandomOverSampler module form imbalanced-learn
1. Instantiate the RandomOverSampler and resample the training data
1. Fit the **original** training data to the random_oversampler model
1. Fit the model using the **resampled training data**
1. Make a prediction using the testing data
1. Print the balanced_accuracy score of the model

## Results

* Machine Learning Model 1:
  * The report details for the logistic regression model successfully predicts labels for the healthy and high-risk loans. however, the effectiveness of the model varies based on the label. we can see that a healthy loan is identified with 100% precision, whereas, high-risk loans are only at 85% precision. The recall for both labels are above 90%, yet healthy loans are 99% and high-risks are only 91%. Nonetheless, the model is far more accustomed to learning healthy loans due to there being over 18,000 instances of it and only 619 high-risk loans. The more exposure to a certain label, the better the model will be at recognizing and recalling it correctly!



* Machine Learning Model 2:
  * In comparison to the logres model WITHOUT oversampled data, we can see similair precision rates, however, the models recall has increased significantly for the high-risk loans. Beforehand, the model had a recall rate of ~ 91% for high-risk loans and now we are seeing similair rates for both healthy and high risk loans of approximately 99% recall.

## Summary

In summary, running the oversampled data through the logistic regression model, it is apparent that the model is significantly more accurate at predicting high-risk loans. The recall rate for high-risk loans has increased from 91% to 99%. The precision rate for high-risk loans has also increased from 85% to 99%. However, the model has had the most exposure to healthy loans due to there being over 18,000 instances of it and only 619 high-risk loans. The more exposure to a certain label, the better the model will be at recognizing and recalling it correctly!