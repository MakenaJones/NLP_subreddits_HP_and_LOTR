# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: 
### Executive Summary


### Problem Statement
---
Can a model distinguish if a post is from two of the biggest fantasy fandom subreddits, r/lotr and r/harrypotter? What about if there are no easily identifiable key character names or words associated with the respective lores?


### Data
---

Description of data
- 5,000 posts pulled from r/lotr using Pushshift's API. [(source)](https://www.reddit.com/r/lotr/)
- 5,000 posts pulled from r/harrypotter using Pushshift's API. [(source)](https://www.reddit.com/r/harrypotter/)

### Modelling
---
I created and tested 8 classification models in total and scored using different classification metrics. Count Vectorizer and Tfidf Vectorizer were coupled with 4 different classification modelling techniques:

1. Logistic Regression
2. KNN
3. Naive Bayes
4. Random Forest

I checked model performance using accuracy (ie. ratio of correctly classified posts to total number of predictions)as my classification metric since the data contained balanced classes (50% of posts belong to r/lotr and the other 50% to r/harrypotter).

#### Model performance on training/test data
---

The best performing model was a Count Vectorizer paired with a Logistic Regression model as only 2 posts were misclassified.

#### Primary Findings and Conclusions
---

Our best performing model (count vectorizer and logistic regression) was extremely accurate and only missclassified two posts. We can conclude that the two fandoms are indeed very easy to distinguish based purely on the text data that users post. Looking forward, to answer the second part of my problem statement, would have to examine how we can distinguish two posts that do not contain direct references to the respective fandoms and lore. Applications of these models could involve sentiment analysis (ie. seeing how controversy around JK Rowling has affected sentiments of posts in this fandom space) and looking beyond to compare with other fandoms.
