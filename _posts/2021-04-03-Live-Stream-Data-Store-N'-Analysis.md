My last DE project was an intro into how to sequester my own data. Though it was cool to understand the whole data pipeline from ingestion, to transformation to 
analysis, data was static and getting stagnant pretty quickly.

This project's aim was to sequester live streaming data since real-time data gives you access to fresh, current activity. This is highly valuable because it gives 
you access to current response of customers/public to what is out there in the world. Business use case would be if there is a product launch, such as Apple decided 
to launch its own e-vehicle, what would be public's initial response to that. Marketers/Sales team can gauge market potential/fit by tracking and trending responses
on Twitter. 

In this project, I was able to steam fresh tweets into Postgres database using Tweepy's StreamListener. Instead of a new product launch, I filtered the whole world's
tweets on: ** 'vaccine', 'vax', 'Pfizer', 'Moderna', 'Johnson & Johnson' ** because who else is not curious about the vaccine against COVID-19?
