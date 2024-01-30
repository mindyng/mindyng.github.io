# Motivation
I thought it was time to update my LinkedIn profile picture. So I tried to go the economic route by
using AI to help generate current photos. Midjourney seemed to be the way to go since 
AI enthusiasts consider it better than OpenAI's DALL-E. I had initially thought prompting was like
typing into a search bar. However, I soon realized that information retrieval was different than AI or 
Artificial Narrow Intelligence (ANI). I went through several attempts at generating some updated pictures, 
but the given quads made me look much older or not the same gender?? So I was determined to figure out
how to get the model to output what I had intended.

# Insights
Information retrieval is much different because there is a query and then a set up of how it is 
retrieved. A search engine is instructed on what to retrieve and how to order the results. This is how
Google works as well as how eBay's search search engine works. Instructions are based on strict or fuzzy 
matching of query and how articles/webpages/inventory items are tagged. After relevant items are retrieved,
they are ranked according to another set of instructions such as by how closely tied the title/item
description is to the query.

Artificial Intelligence is based on predicting the next word in a response such as the suggested word in 
your phone's texting app or Gmail's compose email feature. Artificial General Intelligence is more powerful
because it does this at scale. Instead of being trained on one user's text or specific use case, ChatGPT's 
Large Language Model (LLM) was trained on all the documents that have existed up to a certain point in time.
So its point of reference is highly diverse, which makes its answers so relatable, so human.

Given the difference, I had to adjust to the new model. So I had to figure out what sort of inputs were
helpful to give to ChatGPT or Midjourney so that the outputs were closer to __reading my mind__.
I went through quite a few GitHub repos and subreddits. I knew that most of these references were tied to 
specific use cases and so were a gamble for more general use. So I came upon some high-level formulae
to help me properly contruct prompts to increase my chances of good results. The formulae follow.

# Recommendations

## ChatGPT Prompt Formulae:

1. Task
2. Content
3. Exemplars (Examples)
4. Persona
5. Format
6. Tone

* These are in descending order of importance.
* Also, not all these need to be included.
* There needs to be iteration to optimize results.

## Midjourney Prompt Formulae:

This is not a strong rule, but following a certain prompt structure helps many people improve their prompting. For example, when relevant, your prompt may include the following elements in the suggested order:

1. Type of image (e.g., a photo, an illustration, a painting, etc.)
2. The main object is described with relevant characteristics (e.g., a mystical woman with flowing hair in an ethereal dress).
3. Other details and surroundings (e.g., in a misty forest, amidst a field of sunflowers).
4. Style details (e.g., fine art photography, in the style of Picasso, etc.).
5. Parameters (aspect ratio, level of stylization, model, etc.)

# [Code](https://nbviewer.org/github/mindyng/2024-Business-Projects/blob/main/prompt-engineering.ipynb)

# Personal Data Growth/Fun Lessons
I am glad I went through this learning process because it helped me understand the AI difference between search
and the break through in general intelligence. Leveraging this to optimize my own workflows as well as 
optimizing business processes would be huge gains.

# Next Iteration
1. Going through more iterations per prompt
2. Include more parameters to tailor model for intended use
3. Use Meta's [Llama](https://github.com/facebookresearch/llama-recipes/blob/main/examples/Prompt_Engineering_with_Llama_2.ipynb?utm_source=twitter&utm_medium=organic_social&utm_campaign=llama&utm_content=video) to
   experiment more with AGI. Meta has big ambitions to scale out open-source AI. So it would be good to extend my learnings such as with:
    a. Chain-Of-Thought: Simply adding a phrase encouraging step-by-step thinking "significantly improves the ability of large language models to perform complex reasoning" 
    b. Self-Consistency: LLMs are probablistic, so even with Chain-of-Thought, a single generation might produce incorrect results. Self-Consistency (Wang et al. (2022)) introduces enhanced accuracy by selecting the most frequent answer from multiple generations (at the cost of higher compute)
    c. Retrieval-Augmented Generation (RAG): the practice of including information in the prompt you've retrived from an external database (Lewis et al. (2020)). It's an effective way to incorporate facts into your LLM application and is more affordable than fine-tuning which may be costly and negatively impact the foundational model's capabilities. This could be as simple as a lookup table or as sophisticated as a vector database containing all of your company's knowledge
