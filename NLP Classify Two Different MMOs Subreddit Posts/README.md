# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & NLP

## Problem Statement
This project aims to predict what two subreddit will a users post go under. Will the Machine Learning model predict the post goes under the Lost Ark subreddit or World of Warcraft subreddit.  We will fit multiple machine learning models against our data to find out which will be the best model to use for predictions. We also aim to study the text data that we captured through transformation such as vectorization. From this transformed data, we can study word trends between the two subreddits and also individually.  We will also look into doing sentimental analysis for our subreddits to see how do users feel.  


## Summary
- What is the best machine learning model to use for predictions.
- How well did our best model do?
- What words are used often in each subreddit and together?
- What are the sentiments toward the subreddits? Positive, Negative, or Neutral?
- Which game would you want to model your own game against?



## Data Dictionary
|Feature|Type|Dataset|Description|
|---|---|---|---|
|title|object|Data Webscraped from subreddits 'lostarkgame' and 'wow'| Text that was made from a user submitted|
|selftext|object|Data Webscraped from subreddits 'lostarkgame' and 'wow'| Text that was made from a user submitting a post into one of the subreddits|
|title_and_selftext|object|Combined text of title and selftext| Combined text data|
|filtered_title_selftext|object|Filtered title_and_selftext|Filtered text data to remove unnecessary keys and characters|
|subreddit|object|Data Webscraped from subreddits 'lostarkgame' and 'wow'| Name of the subreddit post was webscrapped from|
|subreddit_class|int|Classification Column| 1 if the subreddit is 'wow'. 0 if the subreddit is 'lostarkgame'|
|sentiment|object|Data captured using sentimental analysis on filtered_title_selftext|Dictionary of scores calculated from using nltk.|
|sentiment_compound|float|Overall score of sentimental analysis |Compositve score taken out of the dictionary of data in sentiment|
|sentiment_class|object|Classification Data made based on sentiment_compound|Classification of types of sentiment: positive, negative, neutral|


## Conclusion and Recommendations

The best model to classify our our post into the appropriate subreddit will be a logisitic regression model.  Logistic regression have performed the best against our unseen data because their are small number of predictors (our features or words) that are relevant to predicitng the outcome.  There are a few important words that you can easily connect in a linear model to make a prediction. If there were more complex features that interacted with each other in the data, logistic regression would not do a good fit against unseen data. A Decision Tree will do better job in accurately clasifying something with complex interaction since it will break down the data.
|                              | Train Set | Test Set |
|------------------------------|-----------|----------|
| Logistic Regression          | .97       | .82      |
| KNN                          | .99       | .61      |
| Decision Tree Classifier     | .77       | .70      |
| Bagging                      | .80       | .72      |
| Random Forest Classifier     | .78       | .73      |
| Extra Tree Classifier        | .75       | .70      |
| Gradient Boosting Classifier | .61       | .60      |
With our best model, we tried improving it by transforming it with TfidVectorizer and compare it against CountVectorizer where it did 1% better as seen in the test set. There is a small bias-variance tradeoff to improve our score by that much as you see the train set did slighltly worse in TfidfVectorizer.
| Logistic Regression | Train Set | Test Set |
|---------------------|-----------|----------|
| CountVectorizer     | .97       | .82      |
| TfidfVectorizer     | .96       | .83      |

From our transformed data, we learned that both subreddits have mostly a positive feeling in their posts through sentimental analysis.

Using the interpretable coefficeints that our logisitc regression model provided, we can see that these words were also used in overwhelmingly positive comments. For example, the world 'wow' had a coefficient of 2.09. Exponentiating that number we get an iterpretable number of 8.1 which tells us that if your post has the word 'wow' in it, it is 8 times likely to be clasified under the WoW subreddit.
Vice versa, negative coefficients were more likely indicator to be classified under the Lost Ark subreddit. For example, the word 'ark' has a coefficient of -1.52. Exponentiating that number we get 0.21. This tells us that if your post has the word 'ark' in it, it will be 80% less likely to go under the WoW subreddit.

From these coefficients, we filtered them to be found in post and see what class of sentiment they fell under. Is the post they were under positive, neutral, or negative.  Alot of the top logistic regression coefficients were found to be in positive posts.
For example the word 'faction' in the WoW subreddit was founded in 46 different posts; 35 of them were involved in positive posts, 7 of them were neutral, and 2 were negative.  This gives us an idea that 'faction' is something you want in your MMO game.
The word 'server' in the Lost Ark subreddit appeared in 122 posts; 76 were positive, 27 were negative and 19 were neutral.  This tells us that 'server' is an important feature in an MMO game being mentioned a lot, but this game, Lost Ark, might have some problems with it due to the number of negative comments from it.  You definitely would want to have a high priority on this feature if you built an MMO game.

In conclusion, both games are good games to model your future MMO game to. Both have their downsides which you can decide to improve on and have upsides which you want to build similarly to or maybe even evolve the feature.

## What's next?
Future study/research:
- Create a nltk.sentiment.vader library of words for video games to better accurately score posts/reviews on video games.
- Collect and analyze text data of an MMO subreddit when major in game events occur to study what players like and dont like.
- Collect a huge range (~3 years) of text data to better understand or capture any pattern of what cycles an MMO goes through from player  feedback 
