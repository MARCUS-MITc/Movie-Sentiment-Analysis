# Movie-Sentiment-Analysis
Movie review sentiment classification
The purpose of sentiment analysis or classification can vary depending on the specific context and application. However, here are some general areas where it is used:

Understanding customer feedback:
Monitoring social media:
Improving recommendation systems:
Market research:
Content moderation:
Academic research:
Understanding audience reception: Analyze audience sentiment towards movies to gauge their success, identify strengths and weaknesses, and predict future box office performance.
Recommending movies: Build a system that recommends movies based on users' sentiment towards similar films.
Improving social media platforms: Analyze sentiment towards movies on social media to identify and address potential conflicts or negative trends.
Exploring film criticism: Analyze the sentiment of professional critics' reviews to understand their perspectives and identify critical trends.
These are the few applications of Sentiment Classification.

But my motivation to this project is solely to gain knowledge and understanding by doing projects as reading research papers alone does not give me practical knowledge.
# Dataset used
https://ai.stanford.edu/~amaas/data/sentiment/
We have Data present in two different text files *Reviews* and *Labels*
# Data Preprocessing
-- Removing punctuations
-- Prepre data for modelling
-- Removing outliers
Number of reviews after removing outliers:  25000
# Padding sequences
We are padding to ensure the each review of same size,(this is necessary if we are sending input to model in batches, each review batch should be of same size).
We can also chose to not to pad anything, then batch_size sould be set to 1


# Sentiment Network with PyTorch
