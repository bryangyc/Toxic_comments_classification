# Toxic Comments Classification

---

## Introduction

With the increase reliance of text in the world, via social interactions and especially on social media. It has become important to be able to classify text that are toxic. Toxic comments are comments that are rude, disrespectful, or otherwise likely to make someone leave a discussion, or even leaving the social media platform entirely, in turn affecting the business. Worst case scenorio, it may even lead to depression or suicide.

This is a problem that is important to solve, as it can help to improve online interactions.

---

## Data

This is a project to classify toxic comments using machine learning algorithms. The dataset is taken from kaggle. The dataset can be found [here](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge/data). 

The dataset contains 159571 comments and 6 labels. The labels are toxic, severe_toxic, obscene, threat, insult, identity_hate. 

The dataset is imbalanced. The toxic comments are 10% of the total comments. 


The dataset is split into train and test set. The train set contains 127656 comments and the test set contains 31915 comments. The train set is further split into train and validation set. The train set contains 101712 comments and the validation set contains 25944 comments. The dataset is cleaned using regular expressions. The dataset is then vectorized using TF-IDF vectorizer. The dataset is then trained using various machine learning algorithms. The algorithms used are Logistic Regression, Naive Bayes, Random Forest, XGBoost, Support Vector Machine. The best accuracy is obtained using XGBoost. The accuracy obtained is 0.97. The model is then saved using pickle. 

---
## Steps Taken



