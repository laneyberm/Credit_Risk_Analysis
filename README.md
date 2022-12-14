# Credit Risk Analysis

## Project Overview
###  
We’ve been tasked by SellBy with analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

## Resources
- Data Source: LoanStats_2019Q1.csv
- Software: Jupyter Notebook 6.4.8, Python 3.7.13, 
- Library: Imbalanced-learn, Scikit-learn 

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
</i>

## Summary and Recommendations
The table below is the summary results for all the Machine Learning (ML) models. The overall best ML model was the Easy Emsemble with AdaBoost Classifer. It's Balanced Accuracy Score is 0.6879, Precision is 1.00, Sensitivity is 1.00, and F1 is 1.00.

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
<td align="left"><strong>Easy Ensemble AdaBoost Classifier</td>
<td align="right">0.6879</strong></td>
<td align="right">0.88 / 1.00 / 1.00</td>
<td align="right">0.38 / 1.00 / 1.00</td>
<td align="right">0.53 / 1.00 / 1.00</td></strong>
</tr>
</tbody>
</table>

Recommendations:
- 

