# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

This analysis was run to train and evaluate a model to assess loan risk (whether an account is a healthy loan (0) or high risk loan (1)). Data used were the lending actvity and included the loan size, interest rate, borrower ID, debt to income ratio, number of accounts with the financial institution, whether the account has derogatory marks, the total debt, and loan status with a total of 8 columns and 77,536 rows. 

To train and test the model, I split the data available into a training set (75% of original data) and a testing set (25%). The model was was then trained on the data using LogisticRegression which assumes the data is best fit using logistic regresssion and uses Limited-memory Broyden-Fletcher-Goldfarb-Shanno (lbfgs) algorithm. The model then predicts loan status of each of the remaining lending activity record (testing set) and I measure the efficiency using a confusion matrix and a classification report which I discuss in results. 

## Results

* Machine Learning Model 1:
    * Accuracy Score: Overall the model had an accuracy score of 99%. Very slay :) 
    * Precision: 
        * Class 0: 1.00
        * Class 1: 0.84
        * Findings: The model had a 100% precision score for class 0 (healthy loan) and an 84% for class 1 (high-risk loan), meaning all instances predicted as class 0 are correct while 84% of the instances that are predicted as class 1 are actually class 1, suggesting there are some false positives of high-risk loans. 
    * Recall: 
        * Class 0: 0.99
        * Class 1: 0.94
        * Findings: When it comes to recall, the model had a 99% for class 0 and 94% for class 1. The model correctly idenitfied 99% of class 0 instances correctly, and predicted 94% of class 1 instances correctly. 

## Summary

I would recommend this model. The logistic regression model performs very strongly in classifying high risk and healthy loans. It has some error in identifying high-risk loans, predicting false positives or identifying loans to be high risk when they are not. It also predicts some false negatives for high-risk loans but less so. However, the model is near perfect in predicting healthy loans from lending activity and overall it is accurate.


