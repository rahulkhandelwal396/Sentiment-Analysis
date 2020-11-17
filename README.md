# Sentiment Analysis of Twitter data

Code performs Sentiment Analysis of Twitter data using bag-of-words method and standard Machine Learning algorithms using R.

Text Analytics is also known as Natural Language Processing.
DataSource: Twitter API

The correct classification of tweets was obtained via Amazon Mechanical Turk

Amazon Mechanical Turk is an online platform which divides a task into smaller components. People sign up online to do these tasks for a small fee.

Our human intelligence task included 5 people giving rating to the sentiment of a single tweet from -2 as strongly negative to +2 as strongly positive, and the average value of the scores were taken as the rating of the tweets.

Here we used a technique called Bag-Of-Words to transform text into independent variables.

# Task

On the basis of twitter data tweets, predict if a tweet has a negative sentiment or not.

# Sample data

<img src="Sample Data.png" alt="Data"/>

# Methodology

1. Read data using stringsAsFactors = FALSE
2. Create target variable as a factor : Negative where Avg <= -1
3. Convert tweets to Corpus for the purpose of preprocessing
4. Tolower, PlainTextDocument, removePunctuation, removeStopWords 
5. Convert corpus into DocumentTermMatrix
6. Keep words that appear in 0.5% or more of the tweets (removeSparseTerms)
7. Split data into training and testing sets (70-30)
8. Build Classification tree model (~87.88%)
9. Check accuracy of baseline model (~84%)
10. Build randomForest model (88.45%)
