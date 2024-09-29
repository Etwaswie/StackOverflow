# StackOverflow Assistant

StackOverflow is one of the most popular question-and-answer websites related to computer science and programming. A large amount of questions and answers is constantly being posted, however, the quality of these posts is often insufficient.

In this project, we address the problem of increasing StackOverflow answer quality. We aim to develop an assistant that integrates into the forum’s interface, appearing in the input box. It assesses the answer in an online mode while the
user is typing it in.
To assess new answers, we employ machine learning and use StackOverflow historical data to train classification models. The internal task that the models are solving is to predict the amount of user upvotes for an answer given the question it has been posted to.


In `data_analysis.ipynb`, we analyse the dataset and create train/test splits.
In `tfidf_baseline.ipynb`, we train the TF-IDF and logistic regression baseline.
In `transformers_baseline.ipynb`, we train the Transformer-based models.
