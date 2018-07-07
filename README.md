# Non-deep-learning Sentiment Classification #
This analysis uses non-deep-learning algorithms to identify the sentiment of movie reviews. 

## Description ##
The dataset is published on [Kaggle](https://www.kaggle.com/c/word2vec-nlp-tutorial) as a `word2vec` tutorial. The tutorial also used a random forest classifier. I was curious of the performance of less computationally expensive algorithms so I chose logistic regression and Naive Bayes regression. 

My text preprocessing was similar to the tutorial (HTML tags, punctuation, numbers and stopwords were removed) except that I added lemmatization. As to feature construction, I trained a Bag of Words model similar to the tutorial; in addition I used feature hashing to reduce feature space size - going back to my goal to experiment with computationally inexpensive methods. 

## Benchmark ##
Researchers have found that different individuals do not always agree on the sentiment polarity (positive/negative/neutral) of a phrase or a sentence. [This study by Wilson et. al.](https://dl.acm.org/citation.cfm?id=1220619) found a 82% agreement between two individuals in the assignment of phrase-level sentiment polarity. As a result I expect a good algorithm to have approximately 80% sentiment-scoring accuracy. 

At the time of writing the highest AUC score on the public leaderboard is 0.99259 but the leaderboard does not show accuracy. My simple models have ~0.93 AUC and ~0.87 accuracy. 