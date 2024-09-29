## StackOverflow Assistant

StackOverflow is one of the most popular question-and-answer websites related to computer science and programming. A large amount of questions and answers is constantly being posted, however, the quality of these posts is often insufficient.

This project solves the problem of improving the quality of responses in StackOverflow. The goal is to develop an assistant that integrates into the forum interface and is displayed in the input field. It assesses the answer in an online mode while the
user is typing it in.
To access new answers, machine learning is applied and historical StackOverflow data is used to train classification models. The internal task that the models are solving is to predict the amount of user upvotes for an answer given the question it has been posted to.

# Data

The data is taken from kaggle: https://www.kaggle.com/datasets/stackoverflow/stackoverflow.
Data was preprocessed and cleaned up: removal of HTML tags, links, conversion to lowercase, replacement of abbreviations with full forms.

# Binary classification

As the easiest version of the task, we create labeling for binary classification. The
model has to predict whether the answer score is positive or not. Applying this
filter results into 587993 (0.66%) positive, 300366 (0.33%) nonpositive samples
in train subset and 65175 (0.65%) positive, 33588 (0.34%) nonpositive samples
in test subset.

# Metrics

To evaluate the classification results, the following indicators were calculated: accuracy, macro score F1 and weighted score F1.

In `data_analysis.ipynb`, the dataset was analyzed and training/test partitions were created.
In `tfidf_baseline.ipynb`, the TF-IDF and logistic regression baseline were trained.
In `transformers_baseline.ipynb`, the Transformer-based models were trained.
