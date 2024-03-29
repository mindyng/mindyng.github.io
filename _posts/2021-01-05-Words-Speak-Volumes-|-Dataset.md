Pictures of healthcare workers in Contagion PPE and nurses crouched on hospital floors paralyzed from the Pandemic's onslaught say a 1000 words.
Though words speak volume.

I have created a [dataset](https://www.kaggle.com/mindyng/burnout-dataframe-without-credentials) of tweets from nurses chronicling their day-to-day on the frontlines as well as the toll it has had on their mental health and morale.

The dataset will eventually be used to create a sentiment analyzer that would help a hospital director or even a healthcare worker determine whether or not they are currently burnt out or on the path to it. In order to construct a robust dataset, I went after:

* healthcare workers/tweets that were consistently tweeting about their lives on the frontlines
* common hashtags that were associated with healthcare workers' burnout

My criteria have been met in nurse twitter hashtags: #covidnurse, #RN, #nursecovid19, #nursetwitter. And a popular Ontario nurse who gives specific details on how her day has been, what has troubled her, when she has been worn out, why she is worn out has helped enrichen the dataset. Her handle is rn_critcare. Through her tweets I learned common issues faced with healthcare workers as well such as: moral injury and the pressure they face with those they carry (difficult cases they go through on the job). Hence, I included hashtags: #moralinjury, #thosewecarry.

Tweepy library was used to scrape tweets from the web along with two helpful scripts I found on github. I ultimately went with the second script I found because it allowed me to not just scrape hashtags, but handles/users as well. Though the first script allowed me to specify a start time for tweets I wanted, the second scripts' final scrape had current and sufficient numbers of tweets. The modifcations I made to the second script were my Twitter credentials and which users and hashtags I wanted to specify. 

The initial dataframe has timestamp of tweet, tweet ID, actual tweet itself, tweet source, tweet retweet count, and the tweet's favorite count. The only columns needed for training models were actual tweet itself and an eventual target column called 'burnout'. This column will be based on presence of popular words/terms that come from people who are burnt out of heading in that direction. These terms were determined through Exploratory Data Analysis (EDA), which was used to add other columns as features. Before analyzing and adding more features to the dataframe, I filtered out retweets to ensure there is no redundancy.
