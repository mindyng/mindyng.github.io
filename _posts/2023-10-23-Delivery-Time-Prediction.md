## Business Problem:

When it comes to ETA for a service, how long an order takes to arrive at a customer's location is a huge factor in whether or not a customer will choose to order or even come back
as a customer (retention). If the time it takes to deliver is earlier than predicted time then that will sometimes not harm the brand-customer relationship. However, if a package/goods is delivered 
later than the predicted time then customers will be unstatisfied and most likely will churn and seek a competitor for delivery services.

## Metric(s) To Lift:

1. Conversion - Direct
2. Customer Satisfaction (NPS), e.g. less Customer Support tickets / Retention - Stretch

## Hypothesis:

When providing an accurate delivery time prediction, customers are more willing to order/come back to the platform and have less complaints.

## Analysis/Approach:

The task is to predict the delivery time (in seconds) using a dataset that has all the same predictors as the training dataset except for the target variable: delivery time.

The predictors/independent variables were:

* market_id
* store_id
* store_primary_category
* order_protocol
* total_items
* subtotal
* num_distinct_items
* min_item_price
* max_item_price
* total_onshift_dashers
* total_busy_dashers
* total_outstanding_orders
* estimated_order_place_duration
* estimated_store_to_consumer_driving_duration

Only difference between the dataset given to train the model and the dataset used to predict delivery time were delivery time was not in it and an extra feature called platform had
to be taken out.

In order to dig into the problem, first calculated the target variable by calculating the difference between order creation time and time when order delivered to customer. Then went
into univariate and bivariate analyses. 

Univariate analysis could have been isolated to the target variable, but I wanted to see the distribution of each variable in order to see the distribution and detect
outliers that needed to be excluded. 

![nominal_distribution](nom_dist.png)

For bivariate analysis, the focus was on which of the independent variables mostly affected the dependent/target variable even though there were other comparisons calculated.
Multivariate analysis was limited since we wanted to quickly see any possible correlations between features and delivery time.

## Insights:

## Business Recommendation/Impact for Growth:
