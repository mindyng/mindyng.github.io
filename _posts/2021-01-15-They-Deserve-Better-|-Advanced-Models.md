Recent news is not getting any better. 1 in 3 people in LA are infected. Health care workers continue to suffer through crisis fatigue.

Now hospital directors are sending out incentives - retention bonuses in order to retain nurses and others who are on the fence about leaving healthcare completely. It is understandable and sadly not surprising.
It is getting to be too much for healthcare workers. Nurses, doctors, those on the frontlines deserve better.

I am going to improve my baseline tweet classification model's prediction accuracy by creating [better text vectors](https://www.kaggle.com/mindyng/burnout-advanced-modeling) and learning and implementing some deep learning algorithms. Healthcare workers need to be treated better and earlier before it is too late. 

Global Vectors (GloVE) have been used instead of traditional Count Vectors/TF-IDF because it captures semantic similarity. More specifically, instead of just capturing count/word frequency, it takes into consideration occurrence and co-occurrence. And co-occurrence is not on local statistics (local context information of words), but incorporates global statistics of word co-occurrence to obtain word vectors.

And deep learning architecture (LSTM in our case) has been used due to its ability to do really well on homogeneous features. These sort of features have the same scale and unit of measure such as words in text. Although deep learning architectures are usually used for huge training data sets and when there is time to tune parameters, I wanted to give it a shot since it has been the method of choice for NLP problems.

And my attempt was a success! Turns out that LSTM on GloVE vectors had improvement in minority and majority class' f1-scores, macro average increased and had the least amount of incorrect classifications - 74!!

Next up, deploying/serving model to customers :D
