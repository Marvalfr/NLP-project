# Project 3: Web APIs & NLP
#### Marva Loyfer

### Problem Statement

This project proposes a classification model that can more accurately identify the subreddit a post belongs to, based only on the title. The explored subreddits AskMen and AskWomen. Both subreddits were created in 2010 and have over 3 million subscribers.
Along with accurately predicting posts' association with subreddits, I also wanted to find the key words that were the best predictors, first for both subreddits combined and then for each separately.

### Executive Summary

In this project, I explore data collected through Reddit's Pushshift API to classify posts to either the AskWomen or AskMen subreddit. The data analyzed consists of the recent 3,000 posts (submissions) from either subreddit as of April 29th and May 1st 2022 (respectively). As the request limit for Reddit's Pushshift API is 100 requests per minute, all of the data for this notebook was collected without issue in under a minute.
In order to classify posts, some initial data cleaning and NLP parsing were required before beginning to model using mostly Count Vectorizers and later TFIDF (Term Frequency Inverse Document Frequency) Vectorizers.

Six different classification models were tested using parameter search methods. All of them exceeded the baseline score (=0.51), but non resulted high accuracy score. The KNN model had the lowest score (=0.57), while the Logistic Regression yielded the most accurate predictions, with either TFIDF Vecotrizer or Count Vetorizer (=0.73 for either one of them).

After running the Logistic Regression model, it was found that the top 20 predictors for both subreddits are common stop words.
    
### Conclusions & Recommendations

The models all scored low in the end. A grid search improved the results, however, and expanding the grid search might result in better results. Additionally, it is worth exploring advanced classification models, such as boosting and Naive Bayes, in order to find the best prediction model.