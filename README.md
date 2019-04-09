# Project 3: Reddit Web API & Classification

## Background Information

The goal of this research was to collect Reddit data from the r/conservative and r/liberal channels, identify frequent terms that were uniquely correlated with each channel, and construct an NLP model capable of differentiating between r/liberal and r/conservative posts.

## Project Summary

#### Data Collection

644 posts were collected from r/conservative and 445 were taken from r/liberal. The posts were pulled using the Reddit API, which rate limits to 25 posts per call and an upper bound of 1,000 posts. For both r/liberal and r/conservative, posts often consisted of hyperlink titles with no body text. As such, another function was built to open the posts page through its permalink, collect all the comments' text through webscraping, and append the comment text as a feature of that post. Also, an additional notebook was created that collects more robust data such as author, upvotes/downvotes, comment depth, and more. However, for the purpose of this project only the comment text was used.

#### Exploratory Data Analysis

The EDA for this project was extensive and comprised the majority of the work on this project. Both the r/liberal and r/conservative posts and data were concatenated into a single DataFrame. As the model is designed to use comment text, all posts without comment text were dropped. The text then went through a stemming and lemming process – ultimately lemming was chosen as the preferred method. The lemmed text was then put through extensive preliminary modeling trials, where 38 different combinations of models were used. The modeling combinations included anywhere from 4-8 combinations of tokenization (Count Vectorizer, Term Frequency-Inverse Document Frequency), ensembling methods (Bagging, AdaBoost), and a latent semantic analysis.

The EDA also examined word count and character count, identifying that r/liberal posts were slightly more verbose with an average of 329 words and 1,938 characters per post as compared the r/conservative's 247 words and 1,429 characters per post. Additionally, an analysis of frequent terms that were uniquely correlated with each channel identified that r/liberal was more likely to use "trump" "republican" "fucking" and "think" while r/conservative was more likely to use "left" "meme" "lol" and "woman."

#### Modeling

Ultimately, the strongest performing models included the Logistic Regression with a TF-IDF, the Multinomial Näive Bayes with a Count Vectorizer and Bagging Ensemble, the Gradient Boosting model, and the latent semantic analysis using the Logistic Regression. Each of these was put through a GridSearchCV to identify the strongest hyperparameters. However, the results were disappointing, revealing at most a 0.02 increase in Cross Valuation Scores.

Finally the top 3 performing models were used to create predictions on a test metric. An ensemble was built where each of these predictions were counted as "votes" and the class with the most votes was the final prediction. However, these results were disappointing, delivering a decrease in overall test score.

The strongest score achieved was a Cross Valuation Score of 0.74 using the Logistic Regression (C=600) with a TF-IDF (n-grams=(1,3)). The baseline score was 0.59.

## Conclusion & Recommendations

The exploratory data analysis revealed some interesting insights about the two channels' verbosity and the unique terms each channel uses. While the model outperformed the baseline (0.74 vs 0.59), the results were somewhat disappointing. It is strongly suggested that future models incorporate at least twice as much data in the training process. Fortunately, the framework of this project would make such analysis relatively easy to produce.