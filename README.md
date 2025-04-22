# Overview
In this assignment, you will explore a dataset containing over one million personal loans originated between 2008 and 2017 on LendingClub. The dataset includes detailed loan characteristics (e.g., interest rate, loan amount), borrower characteristics (e.g., FICO score, income), and loan outcomes (e.g., early default and return). Your task is to analyze the dataset, build linear models, and make predictions of returns on the test set.

# Description
## Requirements
## 1. Exploratory Data Analysis
Perform exploratory data analysis to understand the patterns and relationships within the
dataset. There is no need to repeat the analysis in Assignment 1. Instead, summarize the key
insights from Assignment 1, and any new insights and a second look at the data for Assignment 2.

## 2. Data Preprocessing
### 2.1 Sampling
You are required to implement an expanding-window or rolling-window approach to regularly
updating training and validation sets. You need to justify why you chose either approach.

### 2.2 Handling Missing values
Missing data is present in the dataset. Summarize how you handle the missing values in
Assignment 1, and the changes for Assignment 2, if any.

### 2.3 Feature Engineering
Summarize feature engineering in Assignment 1, and the changes for Assignment 2, if any.

## 3. Model
### 3.1 Linear Regression Model
Fit a simple linear regression model to predict the loan return. Report the in-sample and out-of-sample R-squared.

### 3.2 Classification as a feature
Fit a logistic regression model to predict loan status (i.e., loan_status).
Use the rolling-window or expanding-window approach to tune the decision threshold of the logistic regression.
Apply resampling method, such as random sampling with replacement or SMOTE, to over-sample the minority class, i.e., loans that are charged off.
Report in-sample and out-of-sample model performance, including accuracy, F1 score, and AUC score.
Use the predicted default probability as an engineered feature for the regression problem of returns.

## 4. Predicting on the Test Set
Use your best regression (including the hyperparameters) to predict the outcomes for the test set (lc_loan_test.csv). Replace the values in submission_test.csv for the columns:

return: Your regression predictions for loan returns.
Make sure the predictions match the ‘id’ column to ensure correct evaluation.
For submission details, please refer to Rules section
Evaluation
Submissions are evaluated on R2 between the predicted return and the observed return.
R2=1−(ytrue−ypred)2(ytrue−benchmark)2
where benchmark is 0

Submission File
Refer to 'sample_submission.csv' for your test set predictions. It includes the following columns:

id: Unique loan identifier (to match loans in lc_loan_test)
return: Placeholder for your predictions for loan returns. The column is filled with 0
id,return
1,0.1
2,0.15
3,-0.1
etc.
