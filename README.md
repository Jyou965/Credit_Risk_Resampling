# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
Credit risk data samples are inherently imbalanced as risky loans are usualy a small portion of the overall porfolio.  As such, machine learning models trained with regularly distributed data is not as effective in preditions of risky loans.  The purpose of the analysis is to improve the predictive effectiveness of the machine learning model by oversampling the training data of risky loans. 

* Explain what financial information the data was on, and what you needed to predict.
We need to predict if a loan is risky ('1') or healthy('0') by using data on loan size, interest rate, borrower income, debt-to-income, number of accounts,derogatory marks and total debt.

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
There are all together 77,536 loans to be predicted, out of which 2,500 or 3.2% are actual risky loans.  The data is skewed toward healthy loans.

* Describe the stages of the machine learning process you went through as part of this analysis.
We went through three stages of machine learning process:
1. Split the Data into Training and Testing Sets
2. Create and predict a Logistic Regression Model with the Original Data
3. Resampled the training data and predicted a Logistic Regression Model with Resampled Training Data

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
- Split the data into training and testing datasets by using train_test_split.
- Created a logistic regressin model.
- Fit the model to traing data and made preditions on test data.
- Generated scores and reports to evaluate the effectiveness of the predictions, including accuracy score, precision score, recall score and f1 score.
- Created a random oversampler model to balance the training data.
- Used the oversampled model to make predictions and generated scores.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Accuracy score: 95.2%
  * Precision score: 85%
  * Recall score: 91%
  * f1 score: 88%

* Machine Learning Model 2:
  * Accuracy score: 99.4%
  * Precision score: 84%
  * Recall score: 99%
  * f1 score: 91%

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
Model 2, the oversampled model works better because both accuracy and f1 scores impoved.  There is a small trade off in precision for greater improvedment in recall score, meaning the oversampled data improved the ability of capturing actual positives by trading off the % of total predictions that are actually true. It is up to the user to decide if recall or precision should be the focus and whether the effectiveness is good enough for his/her purpose.

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
It is more important to predict the '1's, which are risky loans.  And this category is inherently small in the sample data.

If you do not recommend any of the models, please justify your reasoning.
I recommend Model 2 as the recall score is 99%, meaning of all the risky loans, the model captured 99% of them.  To a lender, recall score is more important than precision score and a recall score of 99% is good by my standard.
