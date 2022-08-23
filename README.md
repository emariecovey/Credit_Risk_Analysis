# Credit_Risk_Analysis

## Overview:
The purpose of this analysis was to create machine learning models to predict credit card risk. Data was provided from LendingClub, a peer-to-peer lending services company, and included a credit card credit dataset. Because credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans, models with unbalanced classes were used. Imbalanced-learn and scikit-learn libraries were used to build and evaluate models using resampling.

First, data was oversampled using the RandomOverSampler and SMOTE algorithms, undersampled the data using the ClusterCentroids algorithm, and combination sampled with SMOTEENN algorithm. Next, two machine learning models to reduce bias were compared, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. The results record differences in performance between the models. 

## Results:
 Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.


![Naive random oversampling](https://github.com/emariecovey/Credit_Risk_Analysis/blob/main/Challenge/Results_screenshots/Naive_random_oversampling.png)
![Cluster centroids undersampling](https://github.com/emariecovey/Credit_Risk_Analysis/blob/main/Challenge/Results_screenshots/cluster_centroids_undersampling.png)
![Smoteenn combination sampling](https://github.com/emariecovey/Credit_Risk_Analysis/blob/main/Challenge/Results_screenshots/SMOTEENN_combination_sampling.png)
![Smote oversampling](https://github.com/emariecovey/Credit_Risk_Analysis/blob/main/Challenge/Results_screenshots/SMOTE_oversampling.png)


![Balanced random forest classifier](https://github.com/emariecovey/Credit_Risk_Analysis/blob/main/Challenge/Results_screenshots/Balanced_random_forest_classifier.png)
![Easy emsemble adaboost classifier](https://github.com/emariecovey/Credit_Risk_Analysis/blob/main/Challenge/Results_screenshots/Easy_ensemble_AdaBoost_classifier.png)


## Summary: 

The f1 values (which accounts for both precision and recall) for the over, under, and combination sampled models were all extremely low (.02 and below) when predicting high-risk loans. These models were all very good at predicting low credit risk loans, which led them to having a high accuracy. However, they had very low precision for high-risk loans (0.01), which resulted in a low f1 score. Because of their low f1 values, none of these models should be used.

The f1 values for the two ensemble learning models were higher (.47) when predicting high-risk loans, because they combine multiple models together to build a stronger model. Their precision was .73, so 73% of loans classified as "high risk" were actually high risk. However, their recall for high-risk loans is only .34, meaning that the models only detect 34% of high-risk applicants. Because of the low recall, this is not the best model, and I would suggest looking for another model. Considering that the dataset is so unbalanced (347 high-risk loans to 68,470 low-risk loans, or about 1 in 200), it's possible this is about as good of a model as this data could produce, and we may need to resort to using this model after testing a few other possibilities. 

