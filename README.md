# Credit Risk Analysis
---
## Overview

Lending companies have just mere minutes to decide if lending their money to a new borrower will be a risk for them or not. There are many variables that need to be taken into account when the lending companies are making a decision. Without the ability to quickly analyze all these vaiables and rate the risk level, they risk losing the customer to a competitor. But, just because they have to quickly make a decision does not mean that they should take unnecessary risks. Machine learning algorithms have the power to quickly analyze all the required data points from a credit application and predict if they are a lending risk. What we have done here is take historical lending data, create a model, and train the model. For this model we used `imbalanced-learn` and `scikit-learn`. The model leverages `resampling` for the evaluations of the data. In order to perform the resampling we used the `RandomOverSampler` library and `SMOTE` algorithms. The data was then undersampled using the `clustercentroid` algorithm. The remaining models used a combined approach of oversampling and undersampling the data using smotenn. Finally, we compared two machine learning models that minimize bias: BalancedRandomForestClassifier and EasyEnsembleClassifier.

---

### Results

- #### Naive Random Oversampling results: Our balanced accuracy test it 65%, the precision for the high_risk has a very low positivity at 1% and the recall is 72% 

![](https://github.com/TONY-H83/Credit_Risk_Analysis/blob/main/Images/Screenshot%202023-04-08%20at%208.07.34%20PM.png)
![](https://github.com/TONY-H83/Credit_Risk_Analysis/blob/main/Images/Screenshot%202023-04-08%20at%208.10.44%20PM.png)

- #### When using `SMOTE` for oversampling: the accuracy score is 66%, the precision for the high_risk loans has a low positvity again at 1% and recall is 63% overall.

![](https://github.com/TONY-H83/Credit_Risk_Analysis/blob/main/Images/Screenshot%202023-04-08%20at%208.16.44%20PM.png)
![](https://github.com/TONY-H83/Credit_Risk_Analysis/blob/main/Images/Screenshot%202023-04-08%20at%208.16.52%20PM.png)

- #### Undersampling: balanced accuracy score is 66% overall, the precision is at 1% and the recall is 63% for high risk.

![](https://github.com/TONY-H83/Credit_Risk_Analysis/blob/main/Images/Screenshot%202023-04-08%20at%208.19.31%20PM.png)
![](https://github.com/TONY-H83/Credit_Risk_Analysis/blob/main/Images/Screenshot%202023-04-08%20at%208.19.37%20PM.png)

---

#

- #### Combination(over and undersampling) results: balanced accuracy score is 66% the precision is 99% and the recall is 57% overall 

![](https://github.com/TONY-H83/Credit_Risk_Analysis/blob/main/Images/Screenshot%202023-04-08%20at%208.25.40%20PM.png)
![](https://github.com/TONY-H83/Credit_Risk_Analysis/blob/main/Images/Screenshot%202023-04-08%20at%208.25.48%20PM.png)

- #### Balanced Random Forest Classifier results: the accuracy score is 78% the precision is 99% and the recall is 88% 

![](https://github.com/TONY-H83/Credit_Risk_Analysis/blob/main/Images/Screenshot%202023-04-08%20at%208.28.58%20PM.png)
![](https://github.com/TONY-H83/Credit_Risk_Analysis/blob/main/Images/Screenshot%202023-04-08%20at%208.29.04%20PM.png)

- #### Easy Ensemble AdaBoost Classifier results: the accuracy score is 91.7% the precision is 99% and the recall is 94% 

![](https://github.com/TONY-H83/Credit_Risk_Analysis/blob/main/Images/Screenshot%202023-04-08%20at%208.28.58%20PM.png)
![](https://github.com/TONY-H83/Credit_Risk_Analysis/blob/main/Images/Screenshot%202023-04-08%20at%208.29.04%20PM.png)

---

## Summary

The overall analysis of the credit risks highlighted some interesting results in our testing models. Our first attempt using `resampling` displayed poor results and would not be recommended for predicting a potential lending risk. With an average of only 1% precision accuracy. Overall, the model that used `ensemble classifiers` proved to be much more accurate and should be used to predict credit risk.
