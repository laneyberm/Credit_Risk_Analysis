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
- There are 32 Vine (Paid) reviews.
- There are 12,518,670 non-Vine reviews.

<img src="https://github.com/laneyberm/Credit_Risk_Analysis/blob/main/Resources/images/random_oversampler_results_short.png" width="400">


<b>SMOTE Oversampling</b>
- There are 17 Vine 5 Star reviews.
- There are 7,678,534 non-Vine 5 Star reviews.

<img src="https://github.com/laneyberm/Credit_Risk_Analysis/blob/main/Resources/images/smote_results_short.png" width="400">
  

<b>Undersampling</b>
- There are no Vine most helpful reviews.
- The percentage of non-Vine most helpful reviews were 5 stars is 39%.

<img src="https://github.com/laneyberm/Credit_Risk_Analysis/blob/main/Resources/images/cluster_centroids_results_short.png" width="400">
  

<b>Combination (Over and Under) Sampling</b>
- There are no Vine most helpful reviews.
- The percentage of non-Vine most helpful reviews were 5 stars is 39%.

<img src="https://github.com/laneyberm/Credit_Risk_Analysis/blob/main/Resources/images/smoteenn_results_short.png" width="400">
  

<b>Balanced Random Forest Classifier</b>
- There are no Vine most helpful reviews.
- The percentage of non-Vine most helpful reviews were 5 stars is 39%.

<img src="https://github.com/laneyberm/Credit_Risk_Analysis/blob/main/Resources/images/random_forest_results_short.png" width="400">
  

<b>Easy Ensemble AdaBoost Classifier</b>
- There are no Vine most helpful reviews.
- The percentage of non-Vine most helpful reviews were 5 stars is 39%.

<img src="https://github.com/laneyberm/Credit_Risk_Analysis/blob/main/Resources/images/AdaBoost_results_short.png" width="400">
  

<b>Model Tester</b>
- There are no Vine most helpful reviews.
- The percentage of non-Vine most helpful reviews were 5 stars is 39%.

<img src="https://github.com/laneyberm/Credit_Risk_Analysis/blob/main/Resources/images/bonus.png" width="600">
</i>

## Summary and Recommendations
The summary results for all ML models is shown in Table 1. <strong>The overall best-performing Machine Learning (ML) model was the EasyEnsemble with AdaBoost classifier</strong>. It's Balanced Accuracy Score (Acc) was .9317 (93.17%), which was the highest of any of the models. Precision (Prec), Sensitivity/Recall (Sens), and Harmonic Mean (F1) are shown for the 'High-Risk' (H) and 'Low-Risk' (L) categories, and Average (Avg) over both H &amp; L.

<p dir="auto">Table 1. Comparison of ML Model Performance Metrics</p>
<table>
<thead>
<tr>
<th align="left">Model</th>
<th align="right">Acc</th>
<th align="right">Prec  (H/L/Avg)</th>
<th align="right">Sens (H/L/Avg)</th>
<th align="right">F1 (H/L/Avg)</th>
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
<td align="left">Easy Ensemble AdaBoost Classifier</td>
<td align="right">0.6879</strong></td>
<td align="right">0.88 / 1.00 / 1.00</td>
<td align="right">0.38 / 1.00 / 1.00</td>
<td align="right">0.53 / 1.00 / 1.00</td>
</tr>
</tbody>
</table>

Recommendations:
- 

