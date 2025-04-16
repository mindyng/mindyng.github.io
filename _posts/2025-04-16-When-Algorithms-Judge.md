_My transition into AI Alignment/Safety all started from a LinkedIn recommended post in my feed. A DS/statistician from Anthropic shared about his transition into AI.
He went into how he used his statistical background to do LLM eval's, which led me to dig deeper into what Anthropic was about. In YouTube's recommended videos for 
Anthropic, I bumped into "How Difficult is AI Alignment? - Anthropic Research Salon". And the philosophy, talk about how the LLM should behave versus just building cool 
agents, which has its value, sparked my interest. This then sent me down a whole rabbit hole with what is AI Alignment, bumping into BlueDot Impact's "AI Safety Fundamentals"
course as well as Stanford's insightful and impressive "Intro to AI Alignment" course. I soon joined a Women in AI Safety Hackathon and now here I am, sharing with you that I 
got accepted into Apart Lab Studio to flush out further my Hackathon team's idea! Following is a sneek peak into our blogpost that gives a peek into our Hackathon project and how we want to 
further our research to make a huge impact in AI Alignment!_

# When Algorithms Judge: What we Learned from Examining LLM Decision-Making in the Legal Domain

By: May Reese, Markela Zeneli and Mindy Ng

## Introduction
As developments in AI technology continue to impress, it is increasingly employed in sensitive decision-making contexts, such as hiring, policing and law. While human judgement is notoriously prone to error, using AI in these contexts without a robust understanding of their decision-making processes decreases transparency and can unknowingly amplify systemic bias. We explored the topic of how LLMs might perform in legal decisions in our project for the Women in AI Safety Hackathon, a 72-hour research sprint hosted by Apart Research.

Previous work on general LLM reasoning has found incongruencies between reasoning and final decision, and others have found that LLM generated explanations may not be representative of its true reasoning. Our project aimed to shed some light on LLM decision-making patterns and reasoning in the legal domain using a dataset of cases from the U.S. Supreme Court. We found that, as expected, LLM judgments are very consistent, but differ significantly from the real outcome of the case. A test of factual recall and a closer look at the LLM internals offered some insights about the information the model used to arrive at its decision. See figure 1 for a summary of our process. 

