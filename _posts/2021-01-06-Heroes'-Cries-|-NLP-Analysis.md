## Yada yada yada?

Or is there really something in those tweets that is a common denominator? Let's [check out](https://www.kaggle.com/mindyng/burnout-tweets-analysis) what are major themes and bring it to our attention!

There were some intial statistics that I wanted to do on all tweets in order to get a quick overview of what were common, odd, etc. Specific features I went after were: common words, common # characters, how verbose people were and whether or not punctuations were in heavy use. Other features added on were unique word count, stop word count, url count, mean word length, hashtag count and mention count. This was to see if there were statistics that stuck out or outliers. These particular features were for mere curosity and not used for model building.

One interesting insight was sentiment over time. I was able to see that most dips in sentiment occurred at the end of some months.

In order to separate burnout tweets from non-burnout, I used Textblob's sentiment polarity score. What it does is give a score between -1 to 1 to a string. Anything that is below 0 is negative whereas 0 is neutral. And anything above 0 is a positive sentiment. 

From there, visualizations were created that explored sentiment over time as well as words, pairs of words and groups of three words that were most popular in burntout tweets versus non-burntout tweets. 

Interesting finds were that tweets that were lower in sentiment were usually found towards the latter part of the month. Also, bigrams were the most informative when it came to distinguishing words/phrases between burntout and non-burntout language. Lastly, given that the window of time that my sample is from, good thing to keep in mind is the spike of tweets during holidays (end of the month/in Dec). This could easily skew assessments when comparing volumnes of tweets between days/months.

Now that we got to gain a little insight into our tweets, let's get into some model building and let the machine due some learning from all the tweets!
