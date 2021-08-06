# Housing_Market_Prediction
Using economic data predict housing market trends, more specifically crashes. We also use sentiment analysis using live tweets to track general feelings about housing market and what the general talk around the project is.

## Set Up API
Set up Tweepy with required tokens and access keys. Using Api, we created a function that pulls Tweets from Twitter and does a sentiment analysis of those Tweets. 
![image](https://user-images.githubusercontent.com/79224741/128447083-1a5219a8-487b-4ad1-aa8d-274aceba1b7e.png)

## Keyword search
Created function that allows the input of any keyword (can also be hashtag) and searches a requested amount of Tweets, as related to keyword and number inputed. The output is a list of raw Tweets containing the inputted keyword
![image](https://user-images.githubusercontent.com/79224741/128446635-89bed11c-6730-405c-955b-ba4ffb31f78a.png)

## Sentiment Analysis
Dataframe was created containing Tweets with "positive", "negative", and "neutral" sentiment. Created a function that spits out the count of how many Tweets are in each dataframe
![image](https://user-images.githubusercontent.com/79224741/128447909-65eabce9-8977-45e0-b0d7-452dd8b79d69.png)


