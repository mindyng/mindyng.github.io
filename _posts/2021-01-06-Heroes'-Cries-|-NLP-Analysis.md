## Yada yada yada?

Or is there really something in those tweets that is a common denominator? Let's [check out](https://www.kaggle.com/mindyng/burnout-tweets-analysis) what are major themes and bring it to our attention!

In order to separate burnout tweets from non-burnout, I used Textblob's sentiment polarity score. What it does is give a score between -1 to 1 to a string. Anything that is below 0 is negative whereas 0 is neutral. And anything above 0 is a positive sentiment. 

From there, visualizations were created that explored sentiment over time as well as words, pairs of words and groups of three words that were most popular in burntout tweets versus non-burntout tweets. 

Interesting finds were that tweets that were lower in sentiment were usually found towards the latter part of the month. Also, bigrams were the most informative when it came to distinguishing words/phrases between burntout and non-burntout language. Lastly, given that the window of time that my sample is from, good thing to keep in mind is the spike of tweets during holidays (end of the month/in Dec). This could easily skew assessments when comparing volumnes of tweets between days/months.

Now that we got to gain a little insight into our tweets, let's get into some model building and let the machine due some learning from all the tweets!
