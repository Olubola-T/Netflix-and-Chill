# Netflix-and-Chill
INTRODUCTION

This project is centered on sentiment analysis. Also known as opinion mining, sentiment analysis involves mining text data to detect the sentiments (emotional tone) that they convey.
This branch of machine learning finds wide application in business and entertainment because it is useful for obtaining user feedback, which can then inform business decisions.
It is also useful for analysing public opinion about issues or events.
In this project, the sentiments in some text data were analysed. Thereafter, a classification model was built using a part of the dataset, and this model was used to predict the sentiments in the test data.

DATA COLLECTION

The data used in this project is web data; therefore, the project also involved web scraping. Review data for five movies on the IMDB website (www.imdb.com) was scraped with the requests package and parsed with BeautifulSoup. Selenium is another package that can be used for parsing web data.

DATA PROCESSING

Pandas was used to convert the data obtained from the website into a data frame.
Two schemes, namely tf-idf and bag of words, were used to vectorize the text. This step is important because machine learning models can only handle text as vectors. 
The vectors derived from the tf-idf scheme were used. Vectorization based on tf-idf is considered to be more effective for machine learning because it places emphasis on less common, contextual/topical words (like ‘splendid’, entertaining’, ‘motherhood’, ‘touching’, etc.), which are usually the more important words in a document, while treating common, generic words (like ‘the’, ‘and’, ‘how’, etc.) as less important.

SENTIMENT ANALYSIS

The SentimentIntensityAnalyzer of the nltk package was used to identify the sentiments in the reviews as positive, negative, or neutral, based on their compound polarity scores.

CLASSIFICATION MODEL

Finally, the sklearn package was used to build sentiment analysis model, using support vector classifier and decision tree algorithms.
Having been trained with 70% of the reviews dataset, the model was used to classify test data as negative or positive positive review.

RESULTS

Both algorithms produced similar results. The confusion matrices showed that the algorithm correctly classified all positive reviews, while it wrongly classified all negative reviews (true positives= 0, true negatives=28, false positives= 2, false negatives=0; positive class is negative reviews). This is not surprising, given the imbalanced nature of the training data. The training data contains 97% positive reviews and only 3% negative ones. It is thus underfitted and more effective in identifying positive reviews, while it performs poorly with negative reviews, which it was not well exposed to.

LIMITATIONS

The dataset used in this project is quite small, which explains the underfitting of the model. Another project will be done with a larger dataset.
