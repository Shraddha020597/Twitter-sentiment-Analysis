Tweet Sentiment Analysis for Racist/Sexist Content Detection
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Overview
This project focuses on building a Natural Language Processing (NLP) pipeline to classify tweets as either non-racist/non-sexist (label 0) or racist/sexist (label 1). 
The goal is to develop a robust sentiment analysis system capable of identifying and categorizing potentially harmful content on social media platforms.
I employ a standard NLP workflow including data cleaning, tokenization, stemming, feature engineering (Bag-of-Words), and machine learning classification.

## Dataset
The analysis uses two CSV files: traindata.csv and testdata.csv.
traindata.csv: Contains tweets with pre-assigned sentiment labels (0 or 1).
testdata.csv: Contains unlabeled tweets for model evaluation.

Key Dataset Statistics (from training data):
Total Training Tweets: 31,962
Non-Racist/Non-Sexist Tweets (Label 0): 29,720
Racist/Sexist Tweets (Label 1): 2,242

Note: The dataset exhibits a significant class imbalance, which is an important consideration for model evaluation.

Preprocessing Steps:
Raw tweet data undergoes several cleaning and preparation steps to optimize it for machine learning.
1.  Removal of Twitter Handles
2.  Removal of Special Characters, Numbers, and Punctuation
3.  Removal of Short Words
4.  Tokenization
5.  Stemming

Exploratory Data Analysis (EDA)
Visualizations and statistical analyses were performed to understand the data:
Tweet Length Distribution: Histograms comparing tweet lengths in training and test sets.

Word Clouds:
Overall most frequent words.
Separate word clouds for non-racist/non-sexist tweets.
Separate word clouds for racist/sexist tweets, highlighting specific problematic vocabulary.
Hashtag Analysis: Bar plots showing the top 20 most frequent hashtags associated with both non-racist/non-sexist and racist/sexist tweets.

Feature Engineering
Text data is converted into numerical features using the Bag-of-Words (BoW) model:
CountVectorizer is used to create a matrix where each row is a tweet and each column is a unique word, with values representing word counts.

Modeling
1. Multinomial Naive Bayes
A probabilistic classifier well-suited for text classification.
Accuracy: Approximately 94%

2. Logistic Regression
A linear model used for binary classification.
Accuracy: Approximately 95%
F1-Score: Calculated for a balanced evaluation, especially important due to class imbalance.

Results
Both models demonstrate strong performance in classifying tweets. Logistic Regression slightly outperforms Naive Bayes. 
The confusion matrix for Naive Bayes showed 9056 true negatives (correctly identified non-racist tweets). 
The F1-score for Logistic Regression further indicates good performance in balancing precision and recall.
