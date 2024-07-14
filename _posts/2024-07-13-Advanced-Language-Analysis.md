# Motivation

There have been a couple of conferences lately such as ones from OpenAI and Google that have peaked my interest due to the high expectation to augment/apply AI
in their product offerings. So when Apple, known to be late in the AI front had its annual Worldwide Developer's Conference (WWDC), I wanted to get a pulse of 
people's reactions.

Given that I am writing this on a MacBook Pro and recently got an iPhone, I feel more inclined to be up-to-date with Apple's releases.
I did have the option of just tracking Reddit's WWDC 2024 live megathread or watch [The Verge's](https://www.youtube.com/watch?v=sBXdyUA6A88) condensed version 
of the conference, but that is not as fun as scraping the data and performing NLP analysis on people's reactions. :)

Also, after performing [sentiment analysis on LLM chatbots](https://mindyng.github.io/blog/2024/01/01/Sentiment-Analysis-On-L-L-M-Chatbots), in future iterations, 
I had wanted better topics generated as well as perform sentiment analysis on aspects versus overall comments. 
Lastly, I have been wanting to use a free, open-sourced LLM's API's to generate answers in my notebook.

# Business Insights

The way I approached the analysis was to start at high-level and then go down to the weeds. That is why I started with topic modeling and ended with Aspect-
Based Sentiment Analysis. 

When extracting the most talked about topics from the conference, it turned out that an Apple presenter using competitor's Samsung Notes app
to present was highly joked about. Though noise, did give some insight on what is a great Notes app even if it is not made by company you work for 😂 . 
Despite this top topic, still able to extract much on what people were buzzing about:

<img width="1300" alt="Screenshot 2024-07-14 at 9 39 19 AM" src="https://github.com/user-attachments/assets/9f1612de-5610-4528-bac7-d59e4657c87d">

We see here that the most intriguing things were: Siri's upgrade, iPad calculator app and of course their AI aka 'Apple Intelligence' 😂 integrations.
At the same time, we see that there were some underwhelming sentiments regarding upgrades applied to non-15 base models only, icons/widgets/homescreen personalization
and Apple's brand in general when it comes to solving real problems and being a top innovator. 

Three different approaches in customer feedback was taken: overall comment sentiment (positive, neutral or negative), overall commment emotion 
(which was more granular in sentiment: sadness, fear, anger, surprise, joy and love), aspect based sentiment analysis and finally, on a smaller sample
of comments- Large Language Model was used to determine overall comment sentiment (positive, neutral, negative).

What was found that all 4 performed differently when it came to comparing their scoring with my own human review. LLM outperformed all other sentiment
predictions, but could be done on a small sample. Overall, comments came from conference day and emotion was positive and did not decay with time. 
General sentiment and emotion trends are depicted below. Caveat is that sentiment model accuracy was 20% while emotion model accuracy was at 40%.
At the same time, the sample taken to test model accuracy was only 10 comments.

<img width="1355" alt="Screenshot 2024-07-14 at 9 18 59 AM" src="https://github.com/user-attachments/assets/bc2af1a2-1ba7-4b1d-809f-a83fc3837d18">

<img width="1365" alt="Screenshot 2024-07-14 at 1 55 57 PM" src="https://github.com/user-attachments/assets/21f4c897-9d98-43e8-8ace-523e93ffa6eb">

Also, I compared YouTube versus Reddit engagement, average emotion and average sentiment. 

<img width="737" alt="Screenshot 2024-07-14 at 9 32 05 AM" src="https://github.com/user-attachments/assets/4a631170-c23e-4e2a-8563-e8433628a989">

YouTube was more popular with engagement most likely due to MKBHD channel, but other measurements need improvement.

These coarse views, led me to pursue finer grain sentiment analysis with more precise sentiment scores. Aspect-Based Sentiment Analysis pulls out key 
aspects from a comment and the sentiment tied to it.

<img width="1300" alt="Screenshot 2024-07-14 at 9 33 47 AM" src="https://github.com/user-attachments/assets/18f9acf7-7e37-49ec-94e7-36eb9a16a118">

Now this is what we were after: what was talked about most and the sentiments tied to key aspects.

At the center, we can see the most talked about topics across YouTube and Reddit. The outer layer shows the different sentiments per topic. iOS and 
their competitor, Samsung had negative sentiment mostly tied to it. However, things looked good with iPad only (most likely due to the impressive 
Calculator app). There was positive sentiment for apple, but it was not the dominant emotion.

It looks like from the WWDC conference, iphone, iPad, iOS, android/Samsung (notes), app and features were the most talked about topics. Looks like 
Apple needs to work on their reputation even after catch up with AI frontier.

# Business Recommendations

1. Apple needs to be more of a risk taker
2. Be an innovator and not a copier
3. Research problems people are actually having and solving them
4. Build a watertight strategy and execture feature release faster

Based on the sentiment analysis findings from the WWDC conference, here are some business recommendations for Apple to improve their reputation and address the feedback received:

### 1. **Address Negative Sentiment Towards iOS and Competitors**
- **Enhance iOS Features**: Identify specific pain points in iOS that led to negative sentiment. This could involve improving user interface design, increasing customization options, or enhancing security features.
- **Competitive Analysis**: Conduct a thorough analysis of Samsung and other competitors to understand why they were mentioned negatively and leverage this to highlight areas where Apple can outperform or differentiate itself.

### 2. **Capitalize on Positive iPad Sentiment**
- **Promote iPad Strengths**: Leverage the positive feedback about the iPad, especially the new Calculator app, in marketing campaigns. Showcase the iPad’s strengths in productivity and creativity to attract more users.
- **Expand iPad Ecosystem**: Introduce more apps and features similar to the Calculator app that can enhance the iPad’s utility and appeal. Encourage third-party developers to create innovative apps for the iPad.

### 3. **Improve Overall Sentiment and Brand Perception**
- **Customer Engagement**: Engage with the community through forums, social media, and feedback platforms to address concerns and show that Apple is listening to its customers. Implement changes based on this feedback.
- **Transparency and Communication**: Be transparent about new updates, features, and improvements. Regularly communicate the benefits and innovations in iOS, iPhone, and other Apple products to the public.

### 4. **Leverage AI and Innovation**
- **AI Integration**: Since reputation enhancement after catching up with AI was mentioned, continue to innovate in AI and showcase how these advancements improve user experience. This can include features like improved Siri functionality, enhanced camera capabilities, or AI-driven health features.
- **Highlight AI Success Stories**: Use case studies and testimonials to demonstrate how AI features in Apple products have positively impacted users' lives.

### 5. **Improve Product and Feature Discussions**
- **Targeted Marketing**: Create targeted marketing campaigns that focus on the most talked-about topics like iPhone, iPad, iOS, and new app features. Highlight improvements and new features to shift the sentiment positively.
- **Developer Engagement**: Strengthen relationships with developers by providing more resources, support, and incentives for creating innovative apps and features that can enhance the Apple ecosystem.

### 6. **Enhance Customer Support and Service**
- **Support Channels**: Improve customer support channels to quickly address issues and provide solutions. This can help mitigate negative sentiment and enhance user satisfaction.
- **Community Building**: Foster a strong community of Apple users and enthusiasts who can share positive experiences and tips, thereby improving the overall perception of Apple products.

### Implementation Strategy
- **Short-term**: Launch marketing campaigns focusing on positive aspects, enhance customer support, and start community engagement initiatives.
- **Mid-term**: Develop and release updates addressing the negative feedback on iOS, and introduce new features in the iPad and other products.
- **Long-term**: Continue AI innovation, expand the ecosystem with new apps and services, and maintain a transparent communication strategy.

By taking these steps, Apple can improve its reputation, address negative sentiments, and capitalize on positive feedback to strengthen its position in the market.

# Personal Growth as Data Professional/Fun Lessons

1. LLM API and workarounds (data augmentation, sentiment classification)
- First off, LLM's are versatile winners when it came to having to augment data by replacing words with synonyms and performing sentiment analysis on
overall comments. Then again it has greater foundation of knowledge and bigger context window to handle nuanced/domain-specific questions.

2. BERTopic is a library that really peeked my interest. Last time I tried topic modeling, it was messy and not helpful when using LDA. The difference is most likely due to BERTopic being transformer-embeddings based whereas LDA is based on probabilities. I enjoyed the visualizations that helped with interpretation. Below was the most fascinating one for me because it had the different topics and upon hovering and playing with the slider, you can examine different topic and words that make up the topics.

<img width="756" alt="Screenshot 2024-07-14 at 1 54 43 PM" src="https://github.com/user-attachments/assets/e3a8cd12-1c96-4fdc-a5b0-c51104a69907">

<img width="756" alt="Screenshot 2024-07-14 at 1 55 08 PM" src="https://github.com/user-attachments/assets/e2276b75-93f2-4914-b684-038bad9c6a9f">


4. When it came to determining customer feedback, there was the general approach where a whole comment was scored as positive, neutral and negative.
The sentiment seemed too broad and coarse so I went ahead and tried out an emotion classifier that scored comments into 6 different categories: 
sadness, fear, anger, surprise, joy and love. This was better in theory, but when I audited it with my own review, the sentiment classifier was 20% correct,
emotion classifier was 40% correct, PyABSA was 50% correct and Groq was 80% correct. 😀

3. Last, but not least, I was so happy with using chatGPT 4o (omni) as a code helper (had couple more hiccups than preferred). However, it redeemed itself. When I showed it an image of a table and asked for a non-standard visualization like a stacked bar chart. It produced a sunburst graph that I am quite fond of. I used it one time to showcase user journeys to a business stakeholder and he was impressed by how it captured the answer to his business question in a concise and sophisticated way. 🙂

# [Code and Comments Notebook](https://nbviewer.org/github/mindyng/2024-Business-Projects/blob/main/wwdc-2024-sentiment-analysis_final.ipynb) 

# Next Iteration
1. Data Augmentation with Groq
2. Sentiment/Emotion Classification using HuggingFace models, but fine-tuned on YouTube/Reddit data for greater prediction accuracy
3. Groqcloud at scale. It is fast and free so limit on what it can take is understandable. Try to see if I can hit API differently, e.g. >100 rows
4. Named Entity Recognition (NER) for deeper analysis on for things such as:
* Brand Monitoring:

Track mentions of Apple, Samsung, and their products across various sources.
Identify sentiment associated with each brand or product.

* Competitive Analysis:

Compare the frequency and context of mentions between Apple and Samsung.
Identify key people, locations, or events associated with each company.

* Product Intelligence:

Extract information about specific products (e.g., iPhone, Galaxy) and their features.
Track new product launches and consumer reactions.

* Market Trends:

Identify emerging technologies or features that both companies are focusing on.
Detect shifts in consumer preferences or market dynamics.

* Customer Feedback Analysis:

Automatically categorize customer comments or reviews by product, feature, or issue.
Identify common pain points or praised features for each brand.
