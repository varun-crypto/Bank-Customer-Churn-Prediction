# Bank-Customer-Churn-Prediction

# Introduction

In today’s world, customer churn has become a significant challenge for the banking sector.
This project addresses customer churn in the banking sector by developing a prediction
model and identifying the most important features for influencing customer churn. In this project, three different machine learning models were used Naive Bayes, Decision
Trees, and AdaBoost- for initial analysis.

# Data Description

The dataset is taken from kaggle. It contains around 10000 data points of customer
data from three different countries in Europe. It has 18 distinct columns with a wide range of
customer attributes like demographics, account activity, customer feedback, and other relevant
features.

# Methods

The below figure shows the entire process used for this project to develop a prediction model for customer churn.

![Complete-process (1)](https://github.com/varun-crypto/Bank-Customer-Churn-Prediction/assets/69026838/de6500b5-65c6-41e2-a333-2d3c66fc7069)

# Results

## Initial Model Performance

The table below provides a comparison of the evaluation metrics across the three initial models,
reflecting their performance in predicting customer churn:

<img width="358" alt="image" src="https://github.com/varun-crypto/Bank-Customer-Churn-Prediction/assets/69026838/41499ec2-9620-4684-b919-966abdca6de8">

### Ada Boost Model Confusion Matrix

![image](https://github.com/varun-crypto/Bank-Customer-Churn-Prediction/assets/69026838/28ef1f2c-0e90-4405-bbed-f97a2e0f27c8)

### Ada Boost Model Results after hyperparameter tunning and cross validation

Since AdaBoost model has the best results in initial model 10 fold cross validation was performed
on this model. The following results have been obtained:

Recall : 99.91%
ROC-AUC : 99.97%

These results show that the results of the inital model were true and we can say the AdaBoost
model is performing very well.

Later hyperparameter tunning was done using grid search was used to get the best parameters in
the Adaboost model. The following are the results:

Best hyperparameters for recall and ROC-AUC:

Recall : learning rate: 0.5, n estimators: 300
ROC-AUC : learning rate: 0.01, n estimators: 600

The results of tuned AdaBoost model are:

Recall : 0.999465286472117
ROC-AUC : 0.9998443423208508

These results show that the AdaBoost model is almost achieving a near perfect recall and ROC-AUC
score.

## Feature Importance

Feature selection on the AdaBoost model identified 'Complain' as the most significant predictor
of churn, followed by 'EstimatedSalary' and 'CreditScore' The bar plot visualization of feature
importances provided a clear depiction of each attribute’s influence on the model’s predictions.
Using the AdaBoost model feature importance analysis was performed. From the below figure we
can see that features - 'Complain' and 'EstimatedSalary' followed by 'CreditScore' had the highest
contribution to churn variable.

![image](https://github.com/varun-crypto/Bank-Customer-Churn-Prediction/assets/69026838/88c99f93-1b83-4dff-902b-cda3024c5694)

# Conclusion

In this project prediction of bank customer churn was done using three different machine learning
models. Initially various visualisations were performed to analyse the dataset and compare customer
churn to other features. To overcome class imbalance SMOTE was used in this analysis. Then
afterwards through initial modelling it was observed that AdaBoost model outperformed other two
models - Naive Bayes and Decision Tree, this result was evident from various evaluation metrics
like recall, precision and ROC-AUC scores. since AdaBoost was the best performer ten fold cross
validation was performed to verify the resutls, this cross validation showed that the inital model
results were indeed true. Then through hyperparameter tuning the best parameters were obtained
for AdaBoost model and recall and ROC-AUC scores were give for tuned model which showed a near
perfect results. Finally, feature importance analysis of AdaBoost model revealed that ’Complain’
and ’EstimatedSalary’ were the most important features to determine customer churn.
This AdaBoost model can be used by the banks to identify weather a customer churns or not
by using the customer data. Then later the banks can take appropriate measures to retain their
customers.








