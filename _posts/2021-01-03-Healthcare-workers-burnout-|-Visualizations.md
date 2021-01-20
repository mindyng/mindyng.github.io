The Pandemic has had a toll on society with spikes of severely unhealthy individuals and deaths over a short amount of time. It has caused a hampered health care system, paralyzed economy, social unrest, mistrust of government and increased mental issues. This is where healthcare workers come in and heal. Unfortunately, the demand for care with limited personnel and PPE has taken a toll on those who are supposed to uphold health. Many of them are experiencing crisis fatigue/post-traumatic stress disorder because the oath they made entering into their profession to give the best patient care is near impossible these days. 

Though good patient care is achievable if healthcare workers' health are assessed and proper intervention is in place. The need is clear based on institutions carrying out surveys that went into cause of crisis fatigue and what has helped lessen or mitigate it.

I have [explored](https://www.kaggle.com/mindyng/healthcare-workers-burnout) survey data as graphs for quick visual consumption on specific burnout indicators as well as actitives that have helped healthcare workers.

Afterwords, with these indicators for burnout I used MockaRoo to create a mock dataset. This was used to build a theoretical burnout classification model. The idea was to get the machine learning pipeline set up and feed in actual data at a later date. 

The model was assessed using an F1 score which is the metric of choice for imbalanced datasets. The ideal score is 1 and the best performing model had a score of 0.68. Nearly 30% of cases were misclassified as a false positive. There were no false negatives! Risk of being false always needs to be assessed. The cost of incorrectly diagnosing someone who is burnt out and actually is not is a lower cost than missing someone who is actually burnt out.

This initial exploration allowed me to see from real survey data what the numerical breakdown for burnout causes were and what has relieved anxiety/stress. Also, an intial baseline model was constructed which was a reminder to be attentive to class imbalance and appropriate metric to choose when comparing models.

# Next steps:
One. Scrape actual tweets from nurses, who according to survey data have been the hardest hit healthcare workers. And from their cries on Twitter, perform data analysis.
Two. Build a more accurate NLP classification model for burnout.
