# Credit Risk Analysis using Python with imbalanced-learn and scikit-learn libraries

## Project Overview
###  
We’ve been tasked by SellBy with analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

## Resources
- Data Source: LoanStats_2019Q1.csv
- Software: Jupyter Notebook 6.4.8, Python 3.7.13, 
- Library: PySpark 3.3.1

## Results
How many Vine reviews and non-Vine reviews were there?
- There are 32 Vine (Paid) reviews.
- There are 12,518,670 non-Vine reviews.

<img src="https://github.com/laneyberm/Credit_Risk_Analysis/blob/main/Resources/images/random_oversampler_results.png" width="900">

How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
- There are 17 Vine 5 Star reviews.
- There are 7,678,534 non-Vine 5 Star reviews.

What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
- The percentage of Vine reviews were 5 stars is 53%.
- The percentage of non-Vine reviews were 5 stars is 61%.

<img src="https://github.com/laneyberm/Credit_Risk_Analysis/blob/main/Resources/images/smote_results.png" width="900">

What percentage of Vine most helpful reviews were 5 stars? What percentage of non-Vine most helpful reviews were 5 stars?
- There are no Vine most helpful reviews.
- The percentage of non-Vine most helpful reviews were 5 stars is 39%.

<img src="https://github.com/laneyberm/Credit_Risk_Analysis/blob/main/Resources/images/smoteenn_results.png" width="900">

<img src="https://github.com/laneyberm/Credit_Risk_Analysis/blob/main/Resources/images/random_forest_results.png" width="900">

<img src="https://github.com/laneyberm/Credit_Risk_Analysis/blob/main/Resources/images/AdaBoost_results.png" width="900">

<img src="https://github.com/laneyberm/Credit_Risk_Analysis/blob/main/Resources/images/bonus.png" width="900">

## Summary and Recommendations
Percent of Vine 5 star reviews are 8% lower than non Vine 5 star reviews. Additionally, there are no Vine reviews that are deemed as most helpful. It seems that the Vine program is not focused on the Ebooks category as there are only 32 total reviews. It is understandable as ebooks may take longer for the user to complete than an item from a different category like apparel. 

Recommendations:
- SellBy should increase the incentive for their members to review the ebooks category. Traditionally, the members of the vine program would have helpful reviews for all reviews. If they could tap into this market, they could potentially become sponsered by publishers or franchises. 

