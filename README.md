# SMOTE

## How to Deal with Imbalanced Data using SMOTE?


With libraries like scikit-learn at our disposal, building classification models is just a matter of minutes. However, building models without properly examining the structure of your data can lead to disastrous results.

## The problem with Imbalanced Data
![image](https://miro.medium.com/max/616/1*yFPrRPSONNyngGNbo243Ag.jpeg)


In classification problems, balancing your data is absolutely crucial. Data is said to be imbalanced when instances of one class outnumber the other(s) by a large proportion.

> "Feeding imbalanced data to your classifier can make it biased in favor of the majority class, simply because it did not have enough data to learn about the minority."
    
## What is SMOTE?

Synthetic Minority Over-sampling TEchnique, abbreviated as SMOTE. Just like the name suggests, the technique generates synthetic data for the minority class.

![image](https://miro.medium.com/max/820/1*Hjp5xV1i3x0j1g7AZMKiwQ.png)

SMOTE proceeds by joining the points of the minority class with line segments and then places artificial points on these lines.

![image](https://miro.medium.com/max/820/1*nHwVl6AgcP_ym8RbXuKvSg.png)

Under the hood, the **SMOTE** algorithm works in 4 simple steps:
1. Choose a minority class input vector
2. Find its k nearest neighbors (k_neighbors is specified as an argument in the SMOTE() function)
3. Choose one of these neighbors and place a synthetic point anywhere on the line joining the point under consideration and its chosen neighbor
4. Repeat the steps until data is balanced

SMOTE is implemented in Python using the **imblearn** library.

## Credit Card Fraud Detection: SMOTE in Python

In my notebook, I worked with [this data](https://www.kaggle.com/mlg-ulb/creditcardfraud/downloads/creditcardfraud.zip/3) available at Kaggle.


## End Notes

There are many sampling techniques for balancing data. SMOTE is just one of them. But, there’s no single best technique. Generally, you need to experiment with a few of them before deciding on one. Make sure to check out the resources I attached above to learn about all the sampling techniques.


