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

All experiments were performed on the Stanford IMDB dataset which is a natural language dataset where movie reviews have labels that describe the sentiment of the movie review. This is one of the many datasets used in the original paper Hierarchical Attention Network. There are 8 different classes that describe the sentiment from 0-3 for negative sentiment to 6-10 for positive sentiment, which are mapped down to negative sentiment 0 and positive sentiment 1.
# Data Preprocessing
-- Removing punctuations
-- Prepre data for modelling
-- Removing outliers
Number of reviews after removing outliers:  25000
# Padding sequences
We are padding to ensure the each review of same size,(this is necessary if we are sending input to model in batches, each review batch should be of same size).
We can also chose to not to pad anything, then batch_size sould be set to 1


# Document Classification Comparisons featuring Hierarchical Attention Network
The Hierarchical Attention Network is a novel deep learning architecture that takes advantage of the hierarchical structure of documents to construct a detailed representation of the document. As words form sentences and sentences form the document, the Hierarchical Attention Network�s representation of the document uses this hierarchy in order to determine what sentences and what words in those sentences are most important in the classification of the document as a whole.
![image](https://github.com/MARCUS-MITc/Movie-Sentiment-Analysis/assets/123622512/53b7e02d-e8ad-4cd2-a921-0ba27019db0f)

This model uses two levels of LSTM encoders at the word and sentences level in order to build the word and sentence level representations of the document. The attention mechanism is used to attribute importance at the word and sentence level.

There are two applications of the attention mechanism that attend over of the word level encoder and the sentence level encoder. These allow the model to construct a representation of the document that attribute greater levels of importance to key sentences and words throughout the document.

# Results
![image](https://github.com/MARCUS-MITc/Movie-Sentiment-Analysis/assets/123622512/bbeea3ff-dbf2-4268-88be-88f64478faac)

Shown above is the training accuracy achieved during training of the HAN model after 120 thousand training steps on the IMDB dataset where the labels are converted to binary classes. As seen the maximum training accuracy achieved is approximately 64% accuracy.

![image](https://github.com/MARCUS-MITc/Movie-Sentiment-Analysis/assets/123622512/4ec0aea7-2cae-4815-be70-6bf60ac9fcaa)

Shown above is the training loss achieved during training of the HAN model after 120 thousand training steps on the IMDB dataset where the labels are converted to binary classes. The training loss seems to be steadily decreasing.

