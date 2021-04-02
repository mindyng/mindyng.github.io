My last DE project was an intro into how to sequester my own data. Though it was cool to understand the whole data pipeline from ingestion, to transformation to 
analysis, data was static and getting stagnant pretty quickly.

This project's aim was to sequester live streaming data since real-time data gives you access to fresh, current activity. This is highly valuable because it gives 
you insight on current customers/public's responses to what is out there in the world. Business use case would be if there is a product launch, such as Apple decided 
to launch its own e-vehicle, what would be public's initial response to that. Marketing/Sales team can gauge market potential/fit by tracking and trending responses
on Twitter. 

In this project, I was able to stream fresh tweets into local my Postgres database using Tweepy's StreamListener. Instead of a new product launch, I filtered the whole world's tweets on: 'vaccine', 'vax', 'Pfizer', 'Moderna', 'Johnson & Johnson' because who is not curious about vaccines against COVID-19 right now? 

Besides the streamed data, what was new and interesting with this project was the ability to create and insert postgres tables all from my Jupyter notebook using Python. No pgAdmin 4 nor TablePlus needed. Though I did end up using CLI (psql) to connect to the right database and pgAdmin 4 to preview the tweet data before doing some basic analysis on the text. 

In the end, was able to see fresh data/current reactions to how the current available vaccines' roll outs have been. Not only do I get relevant data, but filtering the streamed data allowed me to automate the process of doing a search using Twitter's search bar and manually analyzing text to pick up on trends. And this was all done in just 10 blocks of code!
