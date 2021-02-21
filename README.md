# Credit Risk Analysis

## Overview 
Using the credit card credit dataset from LendingClub create six diffrenet machine learning models. Sinve credit risk is an inherently unbalanced classification problem, all models will be trained and evaluated to determine the bestone to use.

## Results

### Oversampling RandomOverSampler
<img src="https://github.com/luisnewmanh/Credit_Risk_Analysis/blob/main/Resources/randomoversampling.PNG">

62% of accuracy. not precise for predicting high risk loans.  sensitivity for prediction of high and low risk are in line with each other. Balance between precision and recall for high risk is minimum.

### Oversampling SMOTE
<img src="https://github.com/luisnewmanh/Credit_Risk_Analysis/blob/main/Resources/smoteoversampling.PNG">

64% of accuracy. not precise for predicting high risk loans.  sensitivity for prediction of high and low risk are somewhat in line with each other. Balance between precision and recall for high risk is minimum. There is an improvement from previos model.

### Undersampling ClusterCentroids
<img src="https://github.com/luisnewmanh/Credit_Risk_Analysis/blob/main/Resources/clusterundersampling.PNG">

49% of accuracy. not precise for predicting high risk loans.  sensitivity for prediction of high and low risk are drifting from each other. Balance between precision and recall for high risk is minimum. Undersampling turned out to be a worse option than oversampling.

### Combination Sampling SMOTEENN
<img src="https://github.com/luisnewmanh/Credit_Risk_Analysis/blob/main/Resources/combinationsampling.PNG">

67% of accuracy. not precise for predicting high risk loans.  sensitivity for prediction of high and low risk are in line with each other. Balance between precision and recall for high risk is minimum. Considering better accuracy, this resampling model is the best.

### Balanced Random Forest Classifier
<img src="https://github.com/luisnewmanh/Credit_Risk_Analysis/blob/main/Resources/randomforest.PNG">

65% of accuracy. greatly improved precision for predicting high risk loans. A trade off for precision  in this model is sensitivity, since thet are not in line with each other. Balance between precision and recall is also improved.

### Easy Ensemble Classifier
<img src="https://github.com/luisnewmanh/Credit_Risk_Analysis/blob/main/Resources/easyensamble.PNG">

89% of accuracy. not precise for predicting high risk loans.  this is a sensitive model for predicting high and low risk. Balance between precision and recall for high risk is not the best.

## Summary
Based on the result my recommendation will be to utilize the Easy Ensemble Classifier; given its high sensitivity it is easier to detect high risk loans which is the main goal for the model. The downside is that low risk loans will be tagged as high risk, but  further investigation on a case by case basis will solve the issue. 
