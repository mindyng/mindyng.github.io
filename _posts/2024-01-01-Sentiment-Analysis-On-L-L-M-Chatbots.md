# Motivation

It was not a surprise that OpenAI's ChatGPT was a highlight in 2023 ever since its release in November 2022. 
I am a subscriber to Daliana Liu's Newsletter, The Data Scientist's Diary. In one of her blog posts called 
_"Data scientists' role in the age of LLMs (Large Language Models)"_ she said that even though LLMs seems to be 
a threat to the Data Scientist (DS) profession, there actually is a need for DS to measure LLMs' performance. 
This was reassuring since it seemed like LLMs/Generative AI are taking over the world.

And as a Data Scientist, [defining metrics](https://data-chef.notion.site/Metric-Overview-fe3202bb07624dde85d2d1d8aee3fc8d) 
are key to ensuring that a business is aligned with its mission statement defined through metrics of success.

# Business Recommendations

After performing Exploratory Data Analysis (EDA), wrangling dirty API/NLP data, was able to determine that
the overall sentiment on ChatGPT was most positive, as is evident from news/social media. What was surprising was
that from all the chatbots compared, it was not ChatGPT's competitor, Claude, second in ranking, but Pi. The
assumption was that Claude would be behind since its founders and majority of the early team were from OpenAI,
the company behind ChatGPT and probably helped build out ChatGPT's first features. I believe Pi is an unexpectedly
favorable ChatBot becomes it offers more of the human experience. 

Caveat about conclusion is on limited sample size and not having even sampling from YouTube and Reddit. There is more 
chatter on social media about ChatGPT, but there would have been more volume of data as well as even distribution of 
comments between chat bots. Imbalanced data between chatbots could easily skew conclusions as sentiment per chatbot. One
workaround is to do sentiment by percentage of population. Still though, best to get larger and more even samples.

# [Code](https://github.com/mindyng/2023-Business-Projects/blob/main/sentiment-analysis-on-llm-chatbots.ipynb)

# Business Insights

Another motivation behind doing this sentiment analysis was to have something to complement the usual A/B tests. From my 
experience and common web analyses, user behvior is just measured by their actions.  This can only provide a small 
window into a users' favor/disfavor towards a product offering. Coming from product anlaysis and seeing this limitation,
I wanted to get a more comprehensive view on user's response to a product/updated features.

# Personal Data Growth/Fun Lessons

### Data Collection
I had no idea this project would be so interesting! Starting from data collection, I bumped into this awesome, aspiring DS' 
repo called Complete [Life Cycle of a Data Science Project](https://github.com/achuthasubhash/Complete-Life-Cycle-of-a-Data-Science-Project). 
This began my introduction to scraping web data. Now I have a better understanding of Data Engineers' jobs and I have some
autonomy now if I worked on a lean team. Instead of working off clean, crafted data from Kaggle, I had the power to pick 
my sources and have a better understanding on why data was wonky because I was the one who retrieved the data.

### Data Cleaning
I never missed cleaning text data, but at the same time, it was good to get back into it since it's the closest data to getting a 
pulse on users and also working with it can get tricky. So if I got familiar with it again, then I would be able to wrangle more 
clean data such as financial data cleaned up by a data engineer. 

While refamiliarizing myself, I got to learn about common social media cleanings - translating emoji's/slang and expanding 
abbreviations. This added a whole new layer of complexity to NLP wrangling, but was interesting to implement. 

### Sentiment Scoring
This was a really cool experiment as I tested different sentiment libraries: Vader, Hugging Face's Happy Transformer, TextBlob
and even Google's NL API. I ended up choosing Vader because it specialized in social media data (could handle emoji's and
slang), but also Happy Transformer and Google's NL API lacked context window (did not allow for large commments) and TextBlob 
lacked accuracy when it came to sentiment scoring.

### Visualization
When it came to graphing sentiment, I had to lead with questions that were specifically tied to sentiment. The goal was to extract
words/phrases that were tied to metrics of success and broken down by sentiment. Then would enable sentiment mapping to features 
that had the most ROI.

Realized context was king since unigram and even trigram wordclouds and bar charts lacked signal.

Discovering ScatterText was a game changer and helped me achieve my original goal of graphing something interactive/more complex
than what I can accomplish with Plotly libraries. Although D3.js was the original plan, ScatterText helped me segregate words by sentiment - not just negative, positive and neutral. It allowed me to have a more complex matrix that so I could compare two different chatbots in one: ChatGPT and Pi. 

Another cool thing I wanted to do was topic modeling which I was able to achieve using LSA and t-SNE (visualization helper with high dimensional data). As mentioned before, unigrm/trigrams were not providing enough user signal that spoke of chatbot features, so I thought looking at data at a higher level would be better. I wanted to look at reasons tied to product feature for different sentiments. And LDA helped drive topics and t-SNE helped reduce vectors into a more interpretable graph. Topics and their popularity were visible as well as its proximity/relationship to other topics.

# Next iteration:
* Try to get get a filter to get comments that speak on topics surrounding metrics of succcess.
* Add feature release log to time series graphs to directly compare sentiment to new features coming out.