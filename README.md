# Sentiment_analysis_ChatGPT
Sentiment Analysis of three months of Chat GPT tweets on twitter.

This code does sentiment analysis of tweets on twitter for three months (Jan-Mar 2023) with ChatGPT hastags. The tweets were unlabelled.

After cleaning (Tokenization, Noise-Removal, and Lemmatization of content from each tweet) and analysing each column of the dataset closely, I determined the polarity of each tweet from its content using two different tools: NLTK's TextBlob and VaderSentiment Analysis. 

For evaluating the sentiment score from TextBlob: I first did POS(Part-of-Speech) tagging for each tweet, also done by separating each sentence from individual tweet. The adjectives from each tweet are then separated. The polarity is then calculated using TextBlob based on the adjectives of each tweet. 

For Vader sentiment analysis: The content was cleaned but no punctuations were removed such that the tool can read the sentiments accurately for each tweet. The polarity score was then calculated.

I compared the sentiments from both the tools and visualised if there exist any variation in the frequency of tweet and sentiment value over the three months.

I also created wordclouds of both positive and negative sentiments in the reviews (this was especially useful after separating the adjectives from each tweet).

To do a predictive analysis and train ML models, the data was then split into test and training data.

The training data was converted in a set of vectors using Count Vectorizer.

This was then used to train four ML classification models: Logistical Regression, Multinomial Naive Bayes, Support Vector Machine (SVM), and Random Forest.

K-Fold cross validation was performed on each model (with different metrics).

F1 Score, Recall, and Average precision scores are used to determine the best perfoming model, which turned out to be SVM and Logistic Regression. I visualised the average scores for each of these models. 

I finally performed a prediction for some tweets using these models. 

([View Notebook Here](https://nbviewer.org/github/tgautam16/Sentiment_analysis_ChatGPT/blob/main/ChatGPT-sentiment-analysis.ipynb))


