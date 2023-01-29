# Project 3: Web APIs & NLP
#### Marva Loyfer

### Problem Statement

Israel is a country in the Middle East that was established in 1948 as a homeland for Jewish people. It is the only Jewish-majority country in the world and has a population of over 9 million people. The relationship between Israel and Jewish people around the world is complex, with many diaspora Jews feeling a strong connection to the state and its history, while others may have criticisms of its government and policies. Overall, Israel plays a central role in Jewish identity and culture and is considered by many to be a symbol of Jewish continuity and resilience.

The relationship between Israel and non-Israeli Jews was the inspiration for my project. I used natural language processing (NLP) to analyze the discussions in two subreddits: one dedicated to Israel and the other dedicated to Jewish culture.

### Executive Summary

I analyzed information obtained through Reddit's Pushshift API to categorize posts into either the Israel or Jewish subreddit. The data examined encompasses the most recent 2,000 posts (submissions) from either subreddit as of Thursday morning January 26th. As the limit for Reddit's Pushshift API is 200 requests per minute (with 500 posts/submissions per request), all of the data for this notebook was acquired without any difficulties in under a minute.
To classify posts, some initial data cleaning and NLP processing were necessary before beginning to model using both Count Vectorizers and TFIDF (Term Frequency Inverse Document Frequency) Vectorizers. Seven different classification models were tested using various parameter search techniques and all but one with both types of vectorizer to determine which combination of vectorizer, model type, and hyperparameters produced the most accurate model.
In the end, Random Forest and Logistic Regression yielded the most accurate predictions with similar accuracy scores. I selected the Logistic Regression model using the TFIDF Vectorizer as the transformer/model of preference to classify posts/submissions and address our problem statement.
Based on the Logistic Regression model, it was found that the top 20 predictors of Jewish Subreddit were related to identity and culture, such as different forms of the words Jewish and Antisemism, and three different forms of Hannukkah (which can be explained by the date of data collection). Additionally, there were words related to popular culture, such as Kanye (on December 2022, Kanye West was accused of antisemitic behavior) and Jenna Ortega (star of Wednesday). 
Israel and the IDF were among the top 20 predictors on the Israel Reddit, as well as words related to Israeli politics, like Netanyahu, Lapid, Coalition, and Knesset, and tourism (Tel Aviv).

    
### Conclusions & Recommendations

Based on the Logistic Regression model, it was found that the top 20 predictors of Jewish Subreddit were related to identity and culture, such as different forms of the words Jewish and Antisemism, and three different forms of Hannukkah (which can be explained by the date of data collection). Additionally, there were words related to popular culture, such as Kanye (on December 2022, Kanye West was accused of antisemitic behavior) and Jenna Ortega (star of Wednesday). 
Israel and the IDF were among the top 20 predictors on the Israel Reddit, as well as words related to Israeli politics, like Netanyahu, Lapid, Coalition, and Knesset, and tourism (Tel Aviv).
