# Credit_Risk_Analysis
Predict credit card clients at risk for missing payments.
## Project Overview
 The goal is to find an optimal model to predict credit risk, i.e., clients at risk of missing a payment.  As credit risk is unbalanced (the number of defaults is a small percentage of loan holders) the project will survey serval approaches to managing unbalanced data: oversampling, undersampling, a combination of both. Additionally, we will investigate if improvements can be found by using the Balanced Random Forest or Easy Ensemble classifiers.


## Approach
To find a quality solution the project will test a number of methodologies and then compare the resulting accuracy, recall, and precision. 

Sampling/modeling approaches:

     1. RandomOverSampler / LogisticRegression
     2. SMOTE / LogisticRegression
     3. RandomUnderSampler / LogisticRegression
     4. SMOTEENN / LogisticRegression
     5. BalancedRandomForestClassifier
     6. EasyEnsembleClassifier


## Results
| Approach             | Accuracy | Precision | Recall | Link                                                                                                                |
| :------------------- | :------- | :-------- | :----- | :------------------------------------------------------------------------------------------------------------------ |
| RandomOverSampler    | xx.xx    | xx.xx     | xx.xx  | [RandomOverSampler](https://github.com/goldbala55/surfs_up/blob/main/December_Hawaii_Temperature_Statistics.png)    |
| SMOTE                | xx.xx    | xx.xx     | xx.xx  | [SMOTE](https://github.com/goldbala55/surfs_up/blob/main/December_Hawaii_Temperature_Statistics.png)                |
| RandomUnderSampler   | xx.xx    | xx.xx     | xx.xx  | [RandomUnderSampler](https://github.com/goldbala55/surfs_up/blob/main/December_Hawaii_Temperature_Statistics.png)   |
| SMOTEENN             | xx.xx    | xx.xx     | xx.xx  | [SMOTEENN](https://github.com/goldbala55/surfs_up/blob/main/December_Hawaii_Temperature_Statistics.png)             |
| BalancedRandomForest | xx.xx    | xx.xx     | xx.xx  | [BalancedRandomForest](https://github.com/goldbala55/surfs_up/blob/main/December_Hawaii_Temperature_Statistics.png) |
| EasyEnsemble         | xx.xx    | xx.xx     | xx.xx  | [EasyEnsemble](https://github.com/goldbala55/surfs_up/blob/main/December_Hawaii_Temperature_Statistics.png)         |
  



Overview of the analysis: Explain the purpose of this analysis.

Results: Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.

 ## Resources
 Data: Lending Club provided credit history

 Software: Python 3.7.10, Jupyter Notebook 6.3, pandas 1.2.4, numpy 1.19.5, scikit-learn 0.24.1, imbalanced-learn 0.8.0, Git Bash 4.4.23
