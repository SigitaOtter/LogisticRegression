# Logistic Regression - Project

## Task Description
Analyse dataset, create a logistic regression model for predicting 10-year risk of coronary heart disease (CHD) and calculate the optimal threshold.

## Data Source
Kaggle train dataset from an ongoing cardiovascular study on residents of the town of Framingham, Massachusetts:
https://www.kaggle.com/datasets/christofel04/cardiovascular-study-dataset-predict-heart-disea?select=train.csv

## Results in Short

The goal of modelling was to predict ten year coronary heart disease risk in order to give recommendations to edit lifestyle alerting no more than half the patients.

The following was done to get closer to the goal:
- dataset divided to train and test data 80/20
- Class weights for training data applied to account for 6 times less people in the dataset having CHD
- Elastic net regularisation applied to account for possible multicolinearity and remove unnecessary features
- best parameters for regularization found by applying iterations over parameter grid and cross validation
- Optimal threshold to balance recall and precision applied

The model is able to identify 61% of CHD cases. Although precision is quite low at 31%, the goal to not alert more than half the patients is achieved.

## Attachment List
- LogisticRegressionProject.ipynb - Jupyter Notebook file with calculations, descriptions, modelling, charts and conclusions.
- train.csv - csv file with initial dataset
- requirements.txt - versions and libraries used
