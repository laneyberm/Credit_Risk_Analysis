# Credit Risk Analysis

## Project Overview
###  
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, you’ll need to employ different techniques to train and evaluate models with unbalanced classes. Jill asks you to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling. Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, you’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, you’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, you’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once you’re done, you’ll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

Using your knowledge of the imbalanced-learn and scikit-learn libraries, you’ll evaluate three machine learning models by using resampling to determine which is better at predicting credit risk. First, you’ll use the oversampling RandomOverSampler and SMOTE algorithms, and then you’ll use the undersampling ClusterCentroids algorithm. Using these algorithms, you’ll resample the dataset, view the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

you’ll use a combinatorial approach of over- and undersampling with the SMOTEENN algorithm to determine if the results from the combinatorial approach are better at predicting credit risk than the resampling algorithms from Deliverable 1. Using the SMOTEENN algorithm, you’ll resample the dataset, view the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

Using your knowledge of the imblearn.ensemble library, you’ll train and compare two different ensemble classifiers, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk and evaluate each model. Using both algorithms, you’ll resample the dataset, view the count of the target classes, train the ensemble classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

## Resources
- Data Source: LoanStats_2019Q1.csv
- Software: Jupyter Notebook 6.4.8, Python 3.7.13, 
- Library: Imbalanced-learn library, Scikit-learn library, imblearn.ensemble library

## Results
<b><i>Naive Random Oversampling</b>
- Balanced Accuracy Score is 0.4856
- Precision is 0.99
- Sensitivity is 0.07
- F1 is 0.11

<img src="https://github.com/laneyberm/Credit_Risk_Analysis/blob/main/Resources/images/random_oversampler_results_short.png" width="400">

<b>SMOTE Oversampling</b>
- Balanced Accuracy Score is 0.8388
- Precision is 0.99
- Sensitivity is 0.08
- F1 is 0.14

<img src="https://github.com/laneyberm/Credit_Risk_Analysis/blob/main/Resources/images/smote_results_short.png" width="400">
  
<b>Undersampling</b>
- Balanced Accuracy Score is 0.8388
- Precision is 0.99
- Sensitivity is 0.87
- F1 is 0.92

<img src="https://github.com/laneyberm/Credit_Risk_Analysis/blob/main/Resources/images/cluster_centroids_results_short.png" width="400">
  
<b>Combination (Over and Under) Sampling with SMOTEENN</b>
- Balanced Accuracy Score is 0.8438
- Precision is 0.99
- Sensitivity is 0.86
- F1 is 0.92

<img src="https://github.com/laneyberm/Credit_Risk_Analysis/blob/main/Resources/images/smoteenn_results_short.png" width="400">
  
<b>Balanced Random Forest Classifier</b>
- Balanced Accuracy Score is 0.6830
- Precision is 1.00
- Sensitivity is 1.00 
- F1 is 1.00

<img src="https://github.com/laneyberm/Credit_Risk_Analysis/blob/main/Resources/images/random_forest_results_short.png" width="400">
  
<b>Easy Ensemble AdaBoost Classifier</b>
- Balanced Accuracy Score is 0.6879
- Precision is 1.00
- Sensitivity is 1.00
- F1 is 1.00

<img src="https://github.com/laneyberm/Credit_Risk_Analysis/blob/main/Resources/images/AdaBoost_results_short.png" width="400">
  
<b>Model Tester</b>

<img src="https://github.com/laneyberm/Credit_Risk_Analysis/blob/main/Resources/images/bonus.png" width="600">
 
 <b>Easy Ensemble AdaBoost Classifier with n_estimators of 200</b>
- Balanced Accuracy Score is 0.6929
- Precision is 1.00
- Sensitivity is 1.00
- F1 is 1.00
</i>

## Summary and Recommendations
The table below is the summary results for all the Machine Learning (ML) models. The overall best ML model was the Easy Emsemble with AdaBoost Classifer. It's Balanced Accuracy Score is 0.6879, Precision is 1.00, Sensitivity is 1.00, and F1 is 1.00. In addition to the ML models, we ran a Model Tester with different parameters in n_estimators to see if ther are other conditions that would have a better Machine Learning model. From the model testing, we found that the best model is the Easy Ensemble AdaBoost Classifier with n_estimators of 200. 

<p dir="auto">Table 1. Comparison of ML Model Performance Metrics</p>
<table>
<thead>
<tr>
<th align="left">Model</th>
<th align="right">Balanced Accuracy Score</th>
<th align="right">Precision  (H/L/Avg)</th>
<th align="right">Sensitivity (H/L/Avg)</th>
<th align="right">Harmonic Mean (F1) (H/L/Avg)</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Naive Random Oversampling</td>
<td align="right">0.4856</td>
<td align="right">0.01 / 0.99 / 0.99</td>
<td align="right">0.91 / 0.06 / 0.07</td>
<td align="right">0.01 / 0.11 / 0.11</td>
</tr>
<tr>
<td align="left">SMOTE Oversampling</td>
<td align="right">0.8388</td>
<td align="right">0.01 / 0.99 / 0.99</td>
<td align="right">0.89 / 0.07 / 0.08</td>
<td align="right">0.01 / 0.14 / 0.14</td>
</tr>
<tr>
<td align="left">ClusterCentroids Undersampling</td>
<td align="right">0.8388</td>
<td align="right">0.03 / 1.00 / 0.99</td>
<td align="right">0.81 / 0.87 / 0.87</td>
<td align="right">0.07 / 0.93 / 0.92</td>
</tr>
<tr>
<td align="left">SMOTEEN Over and Undersampling</td>
<td align="right">0.8438</td>
<td align="right">0.03 / 1.00 / 0.99</td>
<td align="right">0.83 / 0.86 / 0.86</td>
<td align="right">0.06 / 0.92 / 0.92</td>
</tr>
<tr>
<td align="left">Balanced Random Forest Classifier</td>
<td align="right">0.6830</td>
<td align="right">0.88 / 1.00 / 1.00</td>
<td align="right">0.37 / 1.00 / 1.00</td>
<td align="right">0.52 / 1.00 / 1.00</td>
</tr>
<tr>
<td align="left"><strong>Easy Ensemble AdaBoost Classifier</strong></td>
<td align="right"><strong>0.6879</strong></td>
<td align="right"><strong>0.88 / 1.00 / 1.00</strong></td>
<td align="right"><strong>0.38 / 1.00 / 1.00</strong></td>
<td align="right"><strong>0.53 / 1.00 / 1.00</strong></td>
</tr>
</tbody>
</table>

Recommendations:
- I would recommend that we do other model testing with ClusterCentroids Undersampling and SMOTEEN Over and Undersampling with different parameters for n_estimators to see if these would be better models to use for Machine Learning for credit card risk.. While these two models have the highest balanced accuracy score, its average precision, sensitivity, and F1 are high but not 1.0, like in the case of the Easy Ensemble AdaBoost Classifer.

