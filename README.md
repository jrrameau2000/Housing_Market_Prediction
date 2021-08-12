# Housing_Market_Prediction
Using economic data predict housing market trends, more specifically crashes. We also use sentiment analysis using live tweets to track general feelings about housing market and what the general talk around the project is.

## Set Up API
Set up Tweepy with required tokens and access keys. Using Api, we created a function that pulls Tweets from Twitter and does a sentiment analysis of those Tweets.

![image](https://user-images.githubusercontent.com/79224741/128447083-1a5219a8-487b-4ad1-aa8d-274aceba1b7e.png)

## Keyword search
Created function that allows the input of any keyword (can also be hashtag) and searches a requested amount of Tweets, as related to keyword and number inputed. The output is a list of raw Tweets containing the inputted keyword.
![image](https://user-images.githubusercontent.com/79224741/128446635-89bed11c-6730-405c-955b-ba4ffb31f78a.png)

## Sentiment Analysis
Dataframe was created containing Tweets with "positive", "negative", and "neutral" sentiment. Created a function that spits out the count of how many Tweets are in each dataframe.
![image](https://user-images.githubusercontent.com/79224741/128447909-65eabce9-8977-45e0-b0d7-452dd8b79d69.png)

## Raw Tweets
The variable "tweet_list" contains a list of the most recent tweets as described by the parameters inputted in the "keyword search."
![image](https://user-images.githubusercontent.com/79224741/128603472-0e05e889-6e52-40b3-9a78-1e0fac755956.png)

## Stopwords
Stopwords were imported from nltk.corpus. We also created a for loop that iterated through each tweet to find words that were frequently mentionned. These words could have been a list of adverbs, hashtags, or verbs that don't add much syntax to the project, for example: "a, #housingmarket, realestate, isn't." The goal in finding frequently mentionned words was to create a custom list of stopwords, so we could find more "valuable" words that are mentionnend when a specifici key word is mentionned.
![image](https://user-images.githubusercontent.com/79224741/128603651-793c7d3e-242a-406f-8785-3f292421a757.png)


## Processing Tweets
Created a function that cleans tweets and removes stopwords.
![image](https://user-images.githubusercontent.com/79224741/128603706-cf6b9d12-49c0-4870-b5ae-75f8b68b39ed.png)


## Wordcloud
After each tweet has been processed and cleaned for stopwords, a wordcloud is generated containing words that showed up often. The goal of the wordcloud is to see what people say when a specific keyword is searched. 
![image](https://user-images.githubusercontent.com/79224741/128603774-fffd84fc-3d0a-40ff-a03b-c432531f670c.png)


## Interest Rates
We imported some public data from Fanny Mac regarding interest rates and margin on housing dating back to 1971. The data contains fixed mortgage rates, adjustable mortgage rates, and margin.
![image](https://user-images.githubusercontent.com/79224741/129269017-30a63395-a99e-4b14-aecb-50cf679b4c08.png)


## Houses Bought
The data from interests rates was later merged with another dataframe containing the number of houses purchased in each region of the US, starting from the 1970s. The data was merged in order to facilitate the view of the dataframe and to also create a linear regression model.
![image](https://user-images.githubusercontent.com/79224741/129269199-d70769b7-5be0-4a14-a262-ed8aef4f8974.png)


## Random Forest Regressor
Using the previously mentionned dataframe, we run a random forest regression to create a predictive model.A random forest is a meta estimator that fits a number of classifying decision trees on various sub-samples of the dataset and uses averaging to improve the predictive accuracy and control over-fitting. The sub-sample size is controlled with the max_samples parameter if bootstrap=True (default), otherwise the whole dataset is used to build each tree. X contained interest rates and margin, and y contained houses bought in the US. According to the result, purchases were mostly related to margin than they were related to housing interest rates.
![image](https://user-images.githubusercontent.com/79224741/129271880-6c6eff46-b9a0-42c2-8fff-b2b08b4ca0fb.png)


## Linear Regression
We also ran a linear regression and concluded that about 48% of the time, the data can can explain the trend in houses bought
![image](https://user-images.githubusercontent.com/79224741/129272075-b09bae4c-07b6-41f9-a4d8-80ffd7e46891.png)
