# Module 12 Report Template

## Overview of the Analysis

In this challenge we were tasked with developing a machine learning model to help predict the overall risk of a determined loan. We worked on a dataset that consists of 77,536 individual loans with 8 features that we used to calculate the risk associated with each loan. Such given features were:

* loan_size
* interest_rate
* borrower_income
* debt_to_income
* num_of_accounts
* derogatory_marks
* total_debt
* loan_status

The following steps were performed in order to build our machine learning model:

1. Separate our data into labels and features, with loan_status being our label and the remaining columns being our features.
2. Our data was splitted into training and testing data sets.
3. We then used a logistic regression model to classify each loan into 'healthy' or 'high-risk' loans.
4. Our model was fitted with our training data.
5. We made our predictions with the test data.
6. Evaluated our model by comparing the predictions with the test labels.
7. Make an additional logistic regression prediction this time with resampled data and generate a confusion matrix and classification report with the results.


## Results

### Machine learning model 1:

* Accuracy: 0.95204 
* Precision
  * Healthy: 1.00
  * High-Risk: 0.85
* Recall
  * Healthy: 0.99
  * High-Risk: 0.91

  ### Machine learning model 2:

  * Accuracy: 0.994502 
* Precision
  * Healthy: 0.99
  * High-Risk: 0.99
* Recall
  * Healthy: 0.99
  * High-Risk: 0.99


## Summary

According to the results provided by our classification report, our initial linear regression model has a 95% overall accuracy when classifying loans into 'healthy' and 'high-risk'. This becomes less impressive when we analyze individually each accuracy: we see that it predicts a loan is healthy when it should classify it as high-risk 9% of the time.

On the other hand, on our resampled data model, we get a classification report with 99% accuracy across the board. This model does a much better job predicting whether a loan is healthy or high-risk.

In conclusion, the advantage of resampling is that you can repeatedly draw small samples from the same population till your model achieves its optimum performance. we can save a lot of time and money by being able to recycle the same dataset, and not having to find new data.


