# Fraud Detection and Anomaly detection on credit card transactions

![](/Images/fraud-credit-card.jpg)

## Important Note

The dataset file size exceed what you can upload in github.
In order to that is necessary to install git lfs (https://git-lfs.github.com/).
Inside the git repository run the following lines:
- git lfs install
- git lfs "*.csv"
- git add .gitattributes
From now on just add, commit, push as usual.

## Content

From kaggle website (https://www.kaggle.com/mlg-ulb/creditcardfraud):

"
The dataset contains transactions made by credit cards in September 2013 by European cardholders.
This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.

It contains only numerical input variables which are the result of a PCA transformation. Unfortunately, due to confidentiality issues, we cannot provide the original features and more background information about the data. Features V1, V2, … V28 are the principal components obtained with PCA, the only features which have not been transformed with PCA are 'Time' and 'Amount'. Feature 'Time' contains the seconds elapsed between each transaction and the first transaction in the dataset. The feature 'Amount' is the transaction Amount, this feature can be used for example-dependant cost-sensitive learning. Feature 'Class' is the response variable and it takes value 1 in case of fraud and 0 otherwise.

Given the class imbalance ratio, we recommend measuring the accuracy using the Area Under the Precision-Recall Curve (AUPRC). Confusion matrix accuracy is not meaningful for unbalanced classification. "

## AUC ROC 

This dataset is highly imbalanced so the usual accuracy or the confusion matrix doesn't tell much on how well the model perform. Just 0.172% of all transactions are fraud.
To assess how well a model fits a dataset, we can look at the following two metrics:
- Sensitivity: true positive rate
- Specificity: true negative rate
The ROC curve (receiver operating characteristic) and AUC (area under the curve) display on a plot this two metrics. 

## Model

- Logistic Regressor
- Random Forests Classifier
- XGBoost
- LightGBM

## Conclusion

- Gradiend Boosting family are the best improvement over Logistic Regression and Random Forests

- XGBoost and LightGBM are similar in their outcome but LightGBM is little bit better not only in performance but also in timing and cpu usage.


