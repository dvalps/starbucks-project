# starbucks-project

Author: Damir Valput

Date: 29 January 2021

Program: Machine Learning Engineer nanodegree, Udacity

This project explores the data provided by Starbucks that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free).

Two different models are developed and evaluated:
- an unsupervised k-means clustering to segment the customers in the database according to their socio-economic characteristics, and
- a supervised binary classifier based on the XGBoost model (a built-in AWS SageMaker algorithm).

The data are contained in the folder called 'data/'.

The code with the accompanying comments can be found in two notebooks:
1. Data_Exploration_Feature_Engineering. - This notebook contains all the code for loading the data, cleaning and pre-processing it, data exploration and visualisation, and feature engineering for both ML models. Additionally, it also contains the implementation of the k-Means customer segmentation model. Lastly, it prepares the features for training and testing the binary classifier.
2. Model_Training. - This notebook focuses on the development of the XGBoost binary classifier that aims to predict successfulness of an offer. It loads the datasets prepared in the previous notebook, uploads them to S3 and develops the XGBoost model, executingt the followig steps: estimator definition, hyperparameter tunning, batch transform, deployment, testing and evaluating the model performance on the test data.

All the data that is needed is contained in the 'data' folder, and all the extra libraries needed to run the code are installed in the provided notebooks using pip.
