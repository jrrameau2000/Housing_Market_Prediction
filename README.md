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

## Raw Tweets
The variable "tweet_list" contains a list of the most recent tweets as described by the parameters inputted in the "keyword search"
![image](https://user-images.githubusercontent.com/79224741/128603472-0e05e889-6e52-40b3-9a78-1e0fac755956.png)

## Stopwords
Stopwords were imported from nltk.corpus. We also created a for loop that iterated through each tweet to find words that were frequently mentionned. These words could have been a list of adverbs, hashtags, or verbs that don't add much syntax to the project, for example: "a, #housingmarket, realestate, isn't." The goal in finding frequently mentionned words was to create a custom list of stopwords, so we could find more "valuable" words that are mentionnend when a specifici key word is mentionned.
![image](https://user-images.githubusercontent.com/79224741/128603651-793c7d3e-242a-406f-8785-3f292421a757.png)


## Processing Tweets
Created a function that cleans tweets and removes stopwords
![image](https://user-images.githubusercontent.com/79224741/128603706-cf6b9d12-49c0-4870-b5ae-75f8b68b39ed.png)


# Wordcloud
After each tweet has been processed and cleaned for stopwords, a wordcloud is generated containing words that showed up often. The goal of the wordcloud is to see what people say when a specific keyword is searched. 
![image](https://user-images.githubusercontent.com/79224741/128603774-fffd84fc-3d0a-40ff-a03b-c432531f670c.png)


## Median Home Price
![image](https://user-images.githubusercontent.com/79435102/129270329-b80357db-4ac6-40d6-a3cf-c7ce17ed0477.png)


![image](https://user-images.githubusercontent.com/79435102/129270548-7c1d566d-abef-4adf-a371-40d5f71c3e35.png)

## Number of Homes Sold (in Millions)

![image](https://user-images.githubusercontent.com/79435102/129270846-2ac17ddc-6144-4ceb-880f-e9d49d29c159.png)

![image](https://user-images.githubusercontent.com/79435102/129271079-d5b7bdf4-8601-4ecc-9f44-bbf54f14f050.png)


## Number of New Homes Sold

![image](https://user-images.githubusercontent.com/79435102/129275317-2603c4b1-73b6-4d26-b189-27f3a2190e79.png)


## Mortgage Appliactions Submitted 

![image](https://user-images.githubusercontent.com/79435102/129275424-a659d574-cabf-4694-be02-a6116b07e3a7.png)

## Deep Learning Model
Understanding the links between multiple economic indicators and their influence on mortgage rates we used 8 datasets
to create this model including Inflation(CPI), Changes in Mortgage Back Securities Prices, Avg Wages, the Fed Funds rate, 
number of houses sold, Unemployment rates, and average adjustable and fixed rated mortgages. 

![DL_Code](https://user-images.githubusercontent.com/78506291/129281775-9fc4dd1e-ac95-4465-b0cf-208cb5413248.PNG) ![DL_Code2](https://user-images.githubusercontent.com/78506291/129281895-5417bd8a-7e4c-41b1-a525-c79473ef92ec.PNG) ![DL_Code3](https://user-images.githubusercontent.com/78506291/129282024-6f5702f3-9d7d-4516-9d2f-2da6714fdd90.PNG)


## Inflation
![Inflation_df](https://user-images.githubusercontent.com/78506291/129278662-92913110-d544-4e80-a5e4-a5bf15997d96.PNG)


## Mortgage Backed Securities
![MBS_df](https://user-images.githubusercontent.com/78506291/129279024-f78471e8-9b1c-450b-9c38-85a81aed247e.PNG)


## Fed Funds Rate
![fed_funds](https://user-images.githubusercontent.com/78506291/129279069-ccb83cc2-d14c-41c7-ba19-29e3bd05accf.PNG)


## All Dataframes Combined
![Library_data](https://user-images.githubusercontent.com/78506291/129279760-c11b5cdf-cbd2-4679-b636-ca3b8368cd01.PNG)
![Combined_df](https://user-images.githubusercontent.com/78506291/129279318-ebb2c2ca-1263-4f1d-b87d-15de708c275b.PNG)


## Relationship between Fixed and Adjustable Rate Mortgages
![FvsA_df](https://user-images.githubusercontent.com/78506291/129279731-2e2323cc-b22e-498b-a5c3-f1772c1cee66.PNG)
![FvsA](https://user-images.githubusercontent.com/78506291/129279705-6423043b-8238-48d4-93af-56496ca0572c.PNG)


## Price to Interest Rate Relationship
![PricevsInterest](https://user-images.githubusercontent.com/78506291/129279929-20286908-9c5d-40d8-9054-3b92ce04a03a.PNG)



## Results
![DL_Results](https://user-images.githubusercontent.com/78506291/129279594-029a78bb-61c4-4c5c-9238-fe7d13ff21ee.PNG)
![DL_df](https://user-images.githubusercontent.com/78506291/129282211-06c9f959-b565-4718-9cb3-0a05d282b3b3.PNG)


## Conclusion
Although sentiment may say the US housing market is on the verge of a crash. The data says otherwise. With the Fed keeping 
interest rates astronomically low, there is no reason to predict that prices will go down. Despite other economic indicators 
including rising GDP, rising inflation, low unemployment, more government spending, and wages increasing the Federal Reserve 
is intent on keeping interest low to keep both stock and housing markets on the rise. 


