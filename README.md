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
| Approach             | Accuracy | Precision | Recall | Link                                                                                                                 |
| :------------------- | :------- | :-------- | :----- | :------------------------------------------------------------------------------------------------------------------- |
| RandomOverSampler    | 0.63     | 0.01      | 0.62   | [RandomOverSampler](https://github.com/goldbala55/Credit_Risk_Analysis/blob/main/images/RandomOverSampler.png)       |
| SMOTE                | 0.63     | 0.01      | 0.63   | [SMOTE](https://github.com/goldbala55/Credit_Risk_Analysis/blob/main/images/SMOTE.png)                               |
| RandomUnderSampler   | 0.62     | 0.01      | 0.67   | [RandomUnderSampler](https://github.com/goldbala55/Credit_Risk_Analysis/blob/main/images/RandomUnderSampler.png)     |
| SMOTEENN             | 0.64     | 0.01      | 0.70   | [SMOTEENN](https://github.com/goldbala55/Credit_Risk_Analysis/blob/main/images/SMOTEENN.png)                         |
| BalancedRandomForest | 0.79     | 0.03      | 0.70   | [BalancedRandomForest](https://github.com/goldbala55/Credit_Risk_Analysis/blob/main/images/BalancedRandomForest.png) |
| EasyEnsemble         | 0.93     | 0.09      | 0.92   | [EasyEnsemble](https://github.com/goldbala55/Credit_Risk_Analysis/blob/main/images/EasyEndemble.png)                 |
  
   *The precision and accuracy values listed in the above table are for 'high risk' transactions*

    Observations:
   * In the above results we see that except for the EasyEnsemble the other model's accuracy is mediocre.  While the issues of using accuracy with discreet data is well known, especially with imbalanced data, for a loss prediction model we certainly would flag low accuracy as a concern.
   * Let's examine Recall and Precision metrics. 
    * The precision in all the models is too low and indicates the models are predicting too many false positives, i.e., predicting a late payment/default that is has not occurred.
    * The recall for the EasyEnsemble is solid and indicates the model correctly late payments/defaults at a 92% rate.  All the other models are too low for a scenario involving loss.

## Summary
Only the EasyEnsemble presents as a reasonable model and could be used to flag early potential issues but further analysis and improvements (or alternatives) before using in a production setting.  All the other models are inadequate to use.  They will poorly identify actual loss scenarios while identifying too many false positives - certainly a negative for customer satisfaction.

 ## Resources
 Data: Lending Club provided credit history

 Software: Python 3.7.10, Jupyter Notebook 6.3, pandas 1.2.4, numpy 1.19.5, scikit-learn 0.24.1, imbalanced-learn 0.8.0, Git Bash 4.4.23
