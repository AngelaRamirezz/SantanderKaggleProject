# SantanderKaggleProject
Kaggle Tabular Project using Santander Bank's Customer Satisfaction Kaggle Challenge data
## Overview
Santander Bank wants to priotize their relationships with customers. They proposed a Kaggle challenge, with which they wish to find a system to help identify dissatisfied customers early in their relationship. By doing so they will be able to take corrective steps to imporve the customers experience. Santander Bank presents the data of over 76,000 customers and 370 features. A unique part of this challenge is that Santander Bank intentionally provides wuth anonymized feature to predict if the customers are satisfied. Therefore, most of the features are binary.
This repository contains the approach to obtain the best scores using the best model, to predict customer satisfaction.
The best model resulted in area under the ROC curve between the predicted proability and the observed target AUC=0.85.

## Summary 
### Data
Size: 119.04 MB
76,020 Customers across 371 features

#### Preprocessing/Clean up
First removed ID number, and removed "TARGET" label from the training set.
The training sample was split into train, validation, and test sub-samples.

#### Data Visualization
TARGET Distribution 
![image](https://github.com/user-attachments/assets/e8aa1725-ecba-4549-ada9-2ac8fa7da484)

Distribution of Dissatisfied vs Satisfied customers
![image](https://github.com/user-attachments/assets/9b04be8e-0ae7-42e1-a57a-958522b95663)
![image](https://github.com/user-attachments/assets/546fb079-e505-4868-8148-4576b3fba137)



## Problem Formulation
Models used: 
Logistic Regression

Decision Tree

Random Forst 

## Performance Comparison
ROC curves 

Logistic Regression Model:
![image](https://github.com/user-attachments/assets/b713379b-f9eb-4a35-8027-7f3d7c9e8f9d)

Decision Tree:

![image](https://github.com/user-attachments/assets/554d76ce-593e-4b53-904f-e5a46ba92b5f)

Random Forest:

![image](https://github.com/user-attachments/assets/db2e321b-1dc6-43b1-836d-16ee4cbb3b85)


## Conclusions 
The model that worked best for this particular problem was the Decision Tree. The next best was Logisitc Regression although it had low performance. Random forest had a blocky curve probabily due to errors in data formatting so it was not optimal.

## Future Work 
The next steps to take would be to reattempt formating the data set correctly to obtain a better outcome using the Random Forest model.

## To reproduce results:
Initially, download training data and open in a data frame, for instance in Jupyter Notebook using pandas. Additionally import all essental packages such as the ones listed below. Begin the analytic process by checking the data frame's shape, look for any missing values, and to describe the basic statistics such as count, min and max, mean, standard deviation, and others. Next, for the best results all features should be histogrammed by class (in this case TARGET=1 or TARGET=0) to gain more insite of different distributions in the same variable in each class. Using the histograms we can select which feature are most significant to distinguish the classes. Next, to train select the desired model and separate your data in train_test_split and choose a test size. Run your model and call for accuracy and the classification report. Then visualize these by plotteing the ROC Curve. Lastly, having obtained the best model, run the model on the test data file and create a submission file with the best resulting performance. 

### File Overview:
visulization: Includes data loading, initial analysis, and cleaning tasks. Also contains visualization of data distributions and correlations.

Model1: Trains the first two models, Random Forest, and Logistic Regression

Model2: Trains next model, Desicion Tree

Model3: Contains the attempt at training a Keras model

### Software Setup:
Required packages: 
numpy, pandas, scikit-learn, tensorflow, matplotlib, seaborn, and jupyter


### Data
The data used can be found at https://www.kaggle.com/competitions/santander-customer-satisfaction/data?select=sample_submission.csv 


