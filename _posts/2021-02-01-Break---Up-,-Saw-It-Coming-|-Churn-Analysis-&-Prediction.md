Break-up's are hard. Though there are lessons from any fall out. You take stock of what went wrong/what can be done better the next go around.
What is even better is to foresee red flags in order to corret course. There is no better way to do this in the business
context then to have a machine examine any trends/outliers in those who are loyal (non-churn) versus those who eventually
leave the product (churn).

In my next project, I [examined a fictitious music-streaming company, Sparkify's user data](https://www.kaggle.com/mindyng/churn-prediction/). I explored the data to see what
differences between subscribers and non-subscribers as well as trends between those who stayed on the platform and those
who eventually churnned.

Some feature engineering was performed based on what would seem to differentiate those who do not churn from those who do churn.
For example, average number of hits on certain pages were taken into account. 

Several models were picked as an attempt to best model churn. These included Logistic Regression, Naive Bayes, Suppor Vector 
Machines and XGBoost. The assumption was that XGBoost would do best due to it being popular amongst Kaggle competition winners. 
However, Logistic Regression ended up being the winner. 

Success metrics were f1-score of minority class (churn) and total incorrect predictions. After winning model determined by singling
out the one that had the highest f1-score for churn and lowest amount of wrong classifications, feature importance was determined.

Feature importance reveals which feature in our given X contributed most to our model's prediction. Those with most positive numbers
contributed most to the positive class (1-churn) and those with the lowest numbers contributed most to our 0 class (non-churn). It 
turned out that the paid subscribers who were getting too many advertisements decided to leave the platform. 

Recommended remedies for this is to shorten advertisement lengths or provide no advertisement for first 5 song plays. Also, to 
incentivize those who have stayed on platform longer as paid subscribers, customer success team can provide giftcards. Another
remedy could come in the form of improving recommendation engine to improve engagement/increase sessions time. Lastly, to intervene
on potential churnners, monitoring page activities, number of hits on particular web pages: Add to Playlist, Home, Thumbs up would 
be a strategic move.

In the end, this project was really fun because it stretched my analytic thinking, I was able to dig deep into music streaming, 
understand this industry's unique business processes, do research to become more in tune with its model for operations and success.
