# Twitter Sentiment Analysis
 Analytics Vidhya Hackathon Practice Problem. You can find out more about the problem here: https://datahack.analyticsvidhya.com/contest/practice-problem-twitter-sentiment-analysis/lb
 
 **Problem Statement**
 
The objective of this task is to detect hate speech in tweets. For the sake of simplicity, we say a tweet contains hate speech if it has a racist or sexist sentiment associated with it. So, the task is to classify racist or sexist tweets from other tweets.

Formally, given a training sample of tweets and labels, where label '1' denotes the tweet is racist/sexist and label '0' denotes the tweet is not racist/sexist, your objective is to predict the labels on the test dataset.

**Evaluation Metric**

*F1 Score*  Harmonic mean of precision and recall

**Approach**

**Clean the tweets** - Remove user handles, extract hashtags, expand contractions (i.e. don't - dont, will've - will have etc.), remove punctuations, remove stopwords etc.

**Feature Engineering** - Add length of tweets and a meaning fraction i.e. ratio of lengths of cleaned tweet to actual tweet to the tweet dataframe.

**Create Bag of Words** - Use *Tfidf Vectorizer* for this purpose to weight the documents appropriately. 

**Classification** - Use different classification models like Logistic Regression, Naive Bayes classifier, Support Vector Machines, Decision Trees and Random Forests for classification and find out the best model and use that to make predictions on the test data.

**Results**

Best validation *F1 score* - 0.6812 (Logistic Regression)

Best test *F1 score* - 0.6829 (Support Vector Classifier with linear kernel)
