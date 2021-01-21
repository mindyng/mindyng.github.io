NLP was never something I naturally gravitated towards since it seemed so complex. I rather just deal with numerical datasets instead of the ones full of text. It just looked too messy and complex. However, when I started getting involved with "CoronaWhy" an organization that used algorithms to help classify COVID-19 research papers and created knowledge graphs for information retrieval, my view on NLP started to change. I began to see the power in leveraging computational power to decipher huge bodies of text for a noble cause. And my industry experience at Forethought reinforced NLP as a huge game changer in AI as I was able to use NLU algorithms to automate responses to customer complaints.

Today I am going to wrap up some [NLP modeling](https://www.kaggle.com/mindyng/burnout-modeling) in order to lay down fundamental concepts in NLP. And this will lead to more complex projects and deployments. NLP is no longer a subject matter I hesitate towards, but one I am inclined to tackle head on. So let's go!

Understanding a corpus of text can be daunting but once there is some structure, there can be some clarify and direction in how to interpret a seemingly sea of words. 

We started with the Bag of Words model. This is simply representing a whole corpus as a collection of words without giving words any order/context. So words are simply represented by frequency. And this can be used as a feature in ML. Next up was Topic Modeling which is a statistical manner of clustering similar words. It can examine a set of documents and discovering, based on the statistics of each word, what the topics might be and what each document's balance of topics is. For example, a document about dogs would have appearance of "dog" and "bone" appearing more. Latent Dirichlet allocation (LDA), a generative statistical model was used as it allows sets of observations (words collected into documents) to be explained by unobserved groups (small number of topics).

In my analysis, LDA was performed for the top 4 most frequent words linked to burnout. Results show clusters of words most often associated with most frequent words. LDA separates groups based on ratio of mean and variation between each distinct group.

Next up, I went straight into establishing baseline model predictions. 

Text was vectorized using two methods:

* Count Vectorization
* TF-IDF

Baseline models included:

* Logistic Regression
* Naive Bayes (Multinomial)
* Support Vector Machine

Model prediction accuracy was based on:

* Classification Report
* Confusion Matrix

Count vectorization is more crude than TF-IDF since the former just counts word frequency in a document and does not factor in rare words as much. That is where TF-IDF comes in because it penalizes frequent words so rare words are not discounted. 

As expected TF-IDF outperformed Count Vectorizer representation of text. 

And Logistic Regression was attempted first since it is used often for binary classification especially in business context when deploying models. It is useful because it outputs well-calibrated class probabilities, has unconstrained smooth loss function and works well with Bayesian methods. 

Naive Bayes works well with scalability since the number of parameters is linear and maximum-likelihood training can be done by evaluating closed-form expression (mathematical expression expressed using a finite number of standard operations/no calculus) in linear time.

Support Vector Machines are useful because they do not penalize correctly-labeled examples which is good for generalization. And it gives sparse solutions (uses few variables in the dataset) when using the kernel trick (Non Linear data is projected onto a higher dimension space so as to make it easier to classify the data where it could be linearly divided by a plane) which is nice for scalability.

Out of the three, Logistic Regression performed best. Metrics of success in order from highest to lowest weighted were lowest total incorrect classifications, least amount of false negatives and highest f1-score for minority class.

From there, moved on to non-baseline models aka XGBoost models. This was chosen due to its consistent use as model of choice for Kaggle competition winners. :)

And as no suprise, it became the clear winner. It was tested 4 times (on TF-IDF vectors, Count vectors, SVD features with prior model parameters and SVD features with 1 model parameter). The configuration that came out at the top was XGBoost on TF-IDF vectors!

The reason why XGBoost is so accurate at prediction is because it can train on a lot of data really well to the point of overfitting. Though this is corrected by regularization. Another of its strengths and why it is called Extreme Gradient Boosting is that it pushes the limit of computational resources which means it trains fast!
