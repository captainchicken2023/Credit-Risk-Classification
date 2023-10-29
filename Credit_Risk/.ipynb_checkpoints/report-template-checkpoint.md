# Module 20 Report Template

## Overview of the Analysis

The purpose of this analysis was to evaluate a supervised learning model which predicted whether a given loan application should be classified as high or low risk. The model was trained on historic activity provided by lending services company. 

Inputs evaluated included loan size, borrower income, interest rate, and debt to income ratio. The "y" variable represented the loan status (our target), while the "X" variable represented the features (the numeric inputs needed to reach the target).

I ran two separate analysis, the first based on the original given data, then a second based on "random over-sampling". In each case the data was split into test and training sets, the Logistic Regression Model was setup, and the predictions were made. Finally, I used a Confusion Matrix to analyze the results.

## Results

Brief review of terminology.

* Accuracy:
    * How often the model is correct.
    * Comprised of the ratio of correctly predicted observations to the total number of observations.
    * Accuracy does not communicate how precise a model is.

* Precision:
    * The ratio of correctly predicted positive observations to the total predicted positive observations. 
    * High precision relates to a low false positive rate.
    * In other words, high precision will reduce recall.

* Recall:
    * The ratio of correctly predicted positive observations to all predicted observations for that class. 
    * High recall correlates to a more comprehensive output and a low false negative rate.
    * In other words, high recall will reduce precision


Describing the observed balanced accuracy, precision, and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Accuracy: .95
    High accuracy is misleading. While it did correctly predict a high rate of low-risk applications, the majority of the studied data were low-risk.
    
  * Precision: 1/.85
    We saw a high level of true positive rates in this model, and low false positives.
  
  * Recall: .99/.91
    Falling in line with the above description, recall scores are lower when precision is high, and higher when precision is lower. We witnessed a low number of false positives.


* Machine Learning Model 2: clean sweep at .99
  * Accuracy: .99
  * Precision: .99
  * Recall: .99


## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )


Given the nature of our assignment, it was crucial to ensure that our model could correctly predict when an application was low risk. We do not want to miss an opportunity to provide a loan when conditions are favorable. Both models leaned n the  cautious side and rejected 

At 95% accuracy, the first model appeared to do a very good job predicting which loans will be healthy as opposed to high-risk. However, the model was flawed in that it is lopsided- it contained far more healthy loan entries. If put to use, many high-risk applications could receive approval which may then lead to losses for the loan company. I would not use this model.

Instead, I would opt for the second model. The resampled set had a balance of healthy vs unhealthy loans and the resulting accuracy increased to 99%
