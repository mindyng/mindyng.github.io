## Business Problem:

For a rideshare business like Lyft with stiff competition with UBER, it is important to understand how to maximize each customer's lifetime with their product. By looking into the causes for loyalty and abandonent, Lyft can strategically spend to build features that keep customers engaged and retained. 

- defining LTV
- apply LTV for each driver
- contributors to LTV
- S x D (drivers x rides), how increase rides affect number of drivers?
- how churn, predictive indicators
- attained/retained, retention cohort analysis
- biz rec's

## Metric(s) to Measure/Change:

* LTV
* Churn

## Hypothesis:

By defining, applying and examining contributions to Lyft drivers' LTV, will be able to reduce churn/increase retention.

## Analysis/Approach:

Systematically went through analyzing Lyft's business with high level metrics: LTV, Churn, performing cohort analysis and last but not least, looking at supply and demand.

## Insights:

Used [DuckDB](https://duckdb.org/) again to do a lot of data engineering/data manipulation.

Value of a driver to Lyft over the entire projected lifetime of a driver can be defined as:
[ltv](src="https://github.com/mindyng/mindyng.github.io/assets/12889138/024b0ad4-6ae3-402e-87ea-54f349fc3e7a">)



# Business Growth/Impact for Growth:

* Considering that those contributing most to Lyft’s revenue and hopefully profitable are those who drive a lot during the days they drive, would be best to reward these customers. This would incentivize them/reinforce this strategy of maximizing time out on the road. Possibly free/discounted tickets to events they like would be a good move to increase LTV/retention.
* In order to determine how to increase activity/engagement of churned drivers I would recommend a deeper dive into user journeys and see what behavior brought high LTV/power users from casual user to loyal Lyft driver. Further investigation needed to determine ‘ah-ha’ moment to safeguard against driver/supply drop-off.
* Also, looking into factors contributing to onboard week #15 and #19 would help bring supply to a healthy level to ensure supply is met in marketplace.
Considering that a Lyft lifetime is approximately 2.5 years, at 2 year mark, providing some bonus in monetary or car maintenance reward would make driver feel recognized and supported and most likely carry-on as a Lyft driver.
* To increase retention rates, go heavy on incentives 1 week out from onboarding and whatever incentive/promotion was given for cohort 18 to start driving so quickly as well as for cohort 16 to have overall great retention rates continue to replicate that strategy  since engagement was high during those times.

[Code]()
