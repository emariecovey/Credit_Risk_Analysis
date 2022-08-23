# Credit_Risk_Analysis

## Overview:
The purpose of this analysis was to create machine learning models to predict credit card risk. Data was provided from LendingClub, a peer-to-peer lending services company, and included a credit card credit dataset. Because credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans, models with unbalanced classes were used. Imbalanced-learn and scikit-learn libraries were used to build and evaluate models using resampling.

First, data was oversampled using the RandomOverSampler and SMOTE algorithms, undersampled the data using the ClusterCentroids algorithm, and combination sampled with SMOTEENN algorithm. Next, two machine learning models to reduce bias were compared, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. The results record differences in performance between the models. 

## Results:
 Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

## Summary: 
Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.