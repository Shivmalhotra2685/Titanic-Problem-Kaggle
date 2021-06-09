# Titanic-Problem-Kaggle
My First completion Kaggle  problem - Titanic Survivors
We have used applied machine learning process  for data preparation, model creation , fine tuning and final prediction of the Titanic Survived test dataset.
Accuracy score  of test data set is 0.772
First  we concatenated both test and training data sets to single dataset so that data preparation can be aplied on both training and test dataset
Data Preparation is done by  adding  missing values  using mean / mode values of the variables.
Feature  engineering is applied for Name  variales  to extract titles. First  we use nameparser algoritm but it could  not  extract all the titles. Then we used split function to split the titles to chek if any title is priority or  not.
All Categorical variables  are converted to numercial binary variables and added to main dataset.
The  variables  which are not co-related and contain many unique  values like ticket number, cabin name etc  are removed from dataset.
There are  3 variables with different scale  like Age, Pclass and Fare. These variables are normalized using minmax scaler
We will split the dataset back to training and test dataset.
Spot checking of the various algoritmns are  done on training dataset using cross_val_score algoritms , with kfolds as 10 and metric as accuracy.
Accuracy  of SVC, Randon Forest and Gradient Boost  were  good. Then we checked other  metrices  like precision, recall and f1-score.
As  we can see the  other matrices like predict , recall and f1 score  were good for Algorthm SVC. So we selected SVC algoritm and tried to improve results.
We have fine tuned some of the parameters like max features, n_estimators and learning rate using GridSearchCV algorithm.
Then we saved the model and applied the model on test data  to predict the outcome.
Finally  as per the problem requirement, we created  csv  file for final predictions as per the required parameters.
