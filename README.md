# Credit_Risk_Analysis

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. 

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, the following Machine Learning models were used: Naive Random Oversampling, SMOTE Oversampling, Cluster Centroids Undersampling, SMOTEENN Combination (Over and Under) Sampling, Balanced Random Forest Classifier, and Easy Ensemble AdaBoost Classifier. Performance reports were used to evaluate the models and make a recommendation on whether they should be used to predict credit risk.

## Results

Logistic regression predicts binary outcomes, meaning that there are only two possible outcomes.

There are a number of ways to validate the model and evaluate its performance.

Balanced accuracy is an overall metric used to evaluate how good a binary classifier is at predicting both classes accurately (0 = poor accuracy and 1 = perfect accuracy).

In the imbalanced classification report, a model's precision score is a number 0-1 that represents the accuracy of the model at matching values in the dataset (0 = poor accuracy and 1 = perfect accuracy). A model's recall score is a number 0-1 that represents how well a model accurately predicts the output of a specific input (similarly, 0 = poor precision and 1 = perfect precision).

"In summary, there's a fundamental tension between precision and sensitivity. Highly sensitive tests and algorithms tend to be aggressive, as they do a good job of detecting the intended targets, but also risk resulting in a number of false positives. High precision, on the other hand, is usually the result of a conservative process, so that predicted positives are likely true positives; but a number of other true positives may not be predicted. In practice, there is a trade-off between sensitivity and precision that requires a balancing act between the two."


### Naive Random Oversampling

Balanced Accuracy Score: 

![NRO balanced accuracy](https://github.com/cewarkentin/Credit_Risk_Analysis/blob/main/Images/NRO%20balanced%20accuracy.png)

Imbalanced Classification Report: 

![NRO precision recall](https://github.com/cewarkentin/Credit_Risk_Analysis/blob/main/Images/NRO%20precision%20recall.png)

### SMOTE Oversampling

Balanced Accuracy Score: 

![SMOTE balanced accuracy](https://github.com/cewarkentin/Credit_Risk_Analysis/blob/main/Images/SMOTE%20balanced%20accuracy.png)

Imbalanced Classification Report: 

![SMOTE precision recall](https://github.com/cewarkentin/Credit_Risk_Analysis/blob/main/Images/SMOTE%20precision%20recall.png)

### Cluster Centroids Undersampling

Balanced Accuracy Score: 

![CCU balanced accuracy](https://github.com/cewarkentin/Credit_Risk_Analysis/blob/main/Images/CCU%20balanced%20accuracy.png)

Imbalanced Classification Report: 

![CCU precision recall](https://github.com/cewarkentin/Credit_Risk_Analysis/blob/main/Images/CCU%20precision%20recall.png)

### SMOTEENN Combination (Over and Under) Sampling

Balanced Accuracy Score: 

![SMOTEEN balanced accuracy](https://github.com/cewarkentin/Credit_Risk_Analysis/blob/main/Images/SMOTEEN%20balanced%20accuracy.png)

Imbalanced Classification Report: 

![SMOTEEN precision recall](https://github.com/cewarkentin/Credit_Risk_Analysis/blob/main/Images/SMOTEEN%20precision%20recall.png)

### Balanced Random Forest Classifier

Balanced Accuracy Score: 

![brf balanced accuracy](https://github.com/cewarkentin/Credit_Risk_Analysis/blob/main/Images/brf%20balanced%20accuracy.png)

Imbalanced Classification Report: 

![BRF precision recall](https://github.com/cewarkentin/Credit_Risk_Analysis/blob/main/Images/BRF%20precision%20recall.png)

### Easy Ensemble AdaBoost Classifier

Balanced Accuracy Score: 

![EEC balanced accuracy](https://github.com/cewarkentin/Credit_Risk_Analysis/blob/main/Images/EEC%20balanced%20accuracy.png)

Imbalanced Classification Report: 

![EEC precision recall](https://github.com/cewarkentin/Credit_Risk_Analysis/blob/main/Images/EEC%20precision%20recall.png)

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

There is a bulleted list that describes the balanced accuracy score and the precision and recall scores of all six machine learning models

### Overall

#### The ML models have the following balanced accuracy scores:

- NRO: 0.657
- SMOTE: 0.662
- CCU: 0.545
- SMOTEEN: 0.645
- BRF: 0.789
- EEC: 0.932

The Easy Ensemble AdaBoost Classifier model has the highest balanced accuracy score and the Cluster Centroids Undersampling model has the lowest balanced accuracy score.

#### The ML models have the following precision scores:

- NRO: High Risk - 0.01, Low Risk - 1.00
- SMOTE: High Risk - 0.01, Low Risk - 1.00
- CCU: High Risk - 0.01, Low Risk - 1.00
- SMOTEEN: High Risk - 0.01, Low Risk - 1.00
- BRF: High Risk - 0.03, Low Risk - 1.00
- EEC: High Risk - 0.09, Low Risk - 1.00

All models had high precision for identifying low-risk credit card applicants. The Balanced Random Forest Classifier and Easy Ensemble AdaBoost Classifier models outperformed the rest of the models in terms of precision identifying high-risk credit card applicants. However, the highest precision for the high-risk category was only 0.09, which is very very low.

#### The ML models have the following recall scores:

- NRO: High Risk - 0.71, Low Risk - 0.60
- SMOTE: High Risk - 0.63, Low Risk - 0.69
- CCU: High Risk - 0.69, Low Risk - 0.40
- SMOTEEN: High Risk - 0.72, Low Risk - 0.57
- BRF: High Risk - 0.70, Low Risk - 0.87
- EEC: High Risk - 0.92, Low Risk - 0.94

The Easy Ensemble AdaBoost Classifier model has the highest recall scores for both high-risk and low-risk credit card applicants.

## Summary

Overall, the Easy Ensemble AdaBoost Classifier provided the best predictive model for the given data.
