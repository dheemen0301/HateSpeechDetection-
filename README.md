# HateSpeechDetection-
## Introduction
***
Any sort of content that harshly displays hatred for anything is considered hate speech. It can take the form of either speech or writing. Generally speaking, there are certain unsettling components on social media, especially fake accounts, that spread hatred toward a particular target (it might be a person, a group of people, an ideology, or anything else). Social media platforms struggle with the challenge of identifying and removing offensive content while maintaining the right to free speech. To find texts or writings that indicate hate so that suitable counteractions can be made, hate speech detection is utilised.

## Objectives
***
- To train a machine learning model which can recognize whether the text contains hate speech or not
-  Use the trained classifier on real-world speech to identify hate speech in the text

## Problem Statement
***
Train a classifier that classifies speech into two classes (Hate speech: 1, Non-hate : 0). <a href="https://www.kaggle.com/arkhoshghalb/twitter-sentiment-analysis-hatred-speech">Dataset</a> consisting of various tweets is used to train the model.

## Methodology
***
The method that we are going to use to achieve our objectives are detailed below in steps:
1. **Cleaning data :**
- Removed the Twitter handles associated with the tweets as these do not give any information about the sentiment of the tweet.
- Removal of special characters, symbols, punctuations is also necessary.
- Removal of all the short words ( word length <=3) as they do not convey much information. Stopwords such as I, he, him were also removed using the NLTK library. Decontraction of text was also performed.
- Lowercased the text data. While running the model on the uppercased texts, lower accuracy is obtained. 
- Eliminated the 20 most frequently occurring words along with 20 least frequent words from the dataset, as these helped in concentrating over the words which are of value in the tweet.

2. **Preprocessing data :**
- The words of the cleaned dataset are tokenized using a word tokenizer.
- The word tokens are subjected to stemming and lemmatization, and they are stored.
- After that, we vectorize our data using techniques like BoW and Tf-If (on both stemmed and lemmatized data).

3. **Model :**

The preprocessed data is ready, various models such as Logistic Regression, Decision Tree, XGBoost and Random Forest are used to train the dataset.

**Results :**
***
Out of all the classifiers, the **Random Forest** model over the Tf-Idf Vectorizer on lemmatized tokens turned out to be the best. Accuracy of **0.95** is achieved over the test dataset.

 
 
