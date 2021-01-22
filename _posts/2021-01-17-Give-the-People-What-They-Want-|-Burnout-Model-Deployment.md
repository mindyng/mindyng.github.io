When you build a model, you don't want to have it remain in isolation. It is meant to be used by customers so that their quality of lives improve. So let us serve our [Burnout Classifer](http://192.168.1.174:8501) up!

Initially, I was going to go with Flask to deploy my model, but I consistenly encountered some port issues. And given that I was on a time contraint, I went on a search for something that I could fire up quickly. Let me introduce you to, Streamlit! Instead of having to build something from the ground up, Streamlit allowed me to get a prototype running as quickly as possible. It is Python-based and runs on Tornado and Flask web frameworks. 

The only issues I encountered during deployment was trying to find better animations for a positive sentiment. And that was it. Deployment was very smooth. 

Though upon testing the tool, I realized that the model was not predicting negative tweet at times when it should have. So I checked the deployed model performance metrics against the winning one (XGBoost with GloVe embeddings). Main difference in between the two were in total incorrect predictions (false positives and false negatives). Though I did few live checks and 6/10 times the predictions were accurate. If need be, XGBoost with GloVe embeddings would be next served up model.

Though it was awesome to be able to have a model running in 7 blocks of code and 28-liner Python script.
