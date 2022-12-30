# Metric to Lift:

Decrease number of false transactions leading to inflated revenue metric.

# Business Problem:

Too often fraudalent activity causes misleading spikes to high-level company metrics such as transactions and revenue. In order to mitigate these early on, a model can be built using fraudalent behavior/features and predicting which users are legitimate or not.

# Hypothesis: 

By building a model to predict anomalies to the system, a business can clean up their user base and put in preventative measures to block fraudsters from their system.

# Analysis Approach:

1. Dataset Information
2. Data Visualization
3. Feature Selection
4. Data Balancing
5. Modeling

# Code

[Fraud/Anomaly Detection](https://nbviewer.org/github/mindyng/2022-Business-Projects/blob/main/anomaly-detection.ipynb)

# Recommendation: 

By modeling fraudalent activity, prohibited behavior can be established to prevent company loss in revenue. 

# Conclusion:

The model that won out was K-Nearest Neighbors when it came to which one had the best predictions. Caveat was that due to having to balance the data, synthetic data was generated. Thus, the **accuracy** metric coul not be used to assess models' performance. At the same time, analysis used to generate data that was fed into the models helped give light to several factors leading to fraudalent activity.

# Reference: 
* [Anomaly Detection Basics in Python](https://medium.com/analytics-vidhya/anomaly-detection-in-python-part-1-basics-code-and-standard-algorithms-37d022cdbcff)
