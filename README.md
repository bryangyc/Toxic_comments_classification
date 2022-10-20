# Toxic Comments Classification

---

## Introduction

With the increase reliance of text in the world, via social interactions and especially on social media. It has become important to be able to classify text that are toxic. Toxic comments are comments that are rude, disrespectful, or otherwise likely to make someone leave a discussion, or even leaving the social media platform entirely, in turn affecting the business. Worst case scenorio, it may even lead to depression or suicide.

This is a problem that is important to solve, as it can help to improve online interactions.

---

## Data Overview

This is a project to classify toxic comments using machine learning algorithms. The dataset is taken from kaggle. The dataset can be found [here](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge/data). 

Even though that the data provided contains a train and test set. To further solidify my data science concepts, I have decided to only use the train set only.

The dataset contains 159571 comments and 6 labels. The labels are toxic, severe_toxic, obscene, threat, insult, identity_hate. 

For easier identification through the project, The comments with the labels of either toxic, severe_toxic, obscene, threat, insult and identity_hate, will be named as negative, with the other comments are named positive. If there are any mention of a specific feature, the feature named will be used.

After some investigation, it was found that the dataset is imbalanced. Here is the breakdown of the data imbalance

 | No. of Labels | No. of Rows |
 |:-:|:-:|
 | 0 | 145,346 |
 | 1 | 6,360 |
 | 2 | 3,480 |
 | 3 | 4,209 |
 | 4 | 1,760|
 | 5 | 385|
 | 6 | 31

During the EDA, it

The data was further cleaned by the following methods:

1. Remove punctuation
2. Remove numbers
3. Remove special characters - for example: emojis
4. Remove HTML tags
5. Removal URL

Countvectorizer was used to showcase the most common words in each feature.

<img src='./charts/plots/word_count_for_each_feature.png'>

Logically, the word "fuck" was most commonly seen in all of the features. This is no surprise, as that word is considered one of the most offensive words in the English language.

---
# Machine Learning


## Neural Network
Due to the multi-label dataset, the sklearn's train test split is unable to be used. An alternative was done via Multi Label Stratified Shuffle Split.



The dataset is split into train and test set. The train set contains 127656 comments and the test set contains 31915 comments. The train set is further split into train and validation set. The train set contains 101712 comments and the validation set contains 25944 comments. The dataset is cleaned using regular expressions. The dataset is then vectorized using TF-IDF vectorizer. The dataset is then trained using various machine learning algorithms. The algorithms used are Logistic Regression, Naive Bayes, Random Forest, XGBoost, Support Vector Machine. The best accuracy is obtained using XGBoost. The accuracy obtained is 0.97. The model is then saved using pickle. 

---
## General Steps Taken
1. EDA
   - The different features were explored to see if there are any missing values.
     - The dataset was found to contain no null values.
   - Further exploration were done to take a look into the features, to see what words tend to show up most in each feature.
     - Logically, the word "fuck" was most commonly see in all of the features, which is also true, as that word is considered as offensive/insultive globally.
2. Data Cleaning
3. 
 
