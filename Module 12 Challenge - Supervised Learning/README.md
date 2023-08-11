# Module 12 Report Template

## Overview of the Analysis

The purpose of this analysis was to produce a predictive model that would successfully identify unhealthy loans, or those at risk of default. Our data set provided several attributes around 77.5k loans and included loan size, interest rate, and several other data points. With this data set I split out the 'status' as the classification value from the rest of the data set. I then split the X and y sets in training and testing data with which I fit into a LogisticRegression model to predict against a testing set. The initial model left room for improvement in successfully predicting unhealthy loans so I oversampled the training data to see how that could improve our models performance. Oversampling the dataset improved the recall but saw a slight decrease in precision.


## Results

*Logistic Regression Model:
  * Accuracy: 99.2%
  * Precision: 85%
  * Recall: 91%

* Oversampled Logistic Regression Model:
  * Accuracy: 99.4%
  * Precision: 84%
  * Recall: 99%

## Summary

While the accuracy of the first model is quite high, the imbalanced data poses the risk that the model just classifies more loans as healthy and isn't actually very good at predicting an unhealthy loan. This point is emphasized by the less-than-ideal precision of 85% which means we are incorrectly identifying healthy loans as unhealthy ones. The recall also leaves room to improve coming in at 91% meaning there are 9% of unhealthy loans we incorrectly predicted.

The model built on the oversampled data set doesn't see meaningful differences in Accuracy and Precision (slightly worse actuaclly) but does see a big improvement in Recall. This means that the model correctly identifies 99% of all unhealthy loans.

The most important ability of a predictive model in this context is to correctly predict unhealthy loans so as to minimize the risk of defaulting customers and loss of money. However, the poor Precision of both models means that we would be losing out on 15% of the predicted "unhealthy" loans/customers who are actually healthy ones. This is a loss of revenue and I believe makes even the oversampled model unfit for use.
If you do not recommend any of the models, please justify your reasoning.
