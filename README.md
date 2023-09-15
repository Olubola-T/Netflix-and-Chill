# Netflix-and-Chill
A sentiment analysis project for movie reviews

This project is centered on sentiment analysis. Also known as opinion mining, sentiment analysis involves mining text data to detect the sentiments (emotional tone) that they convey.
This branch of machine learning finds wide application in business and entertainment because it is useful for obtaining user feedback, which can then inform business decisions.
It is also useful for analysing public opinion about issues or events.
The data used in this project is web data; therefore, the project also involved web scraping. Movie review data from the IMDB website (www.imdb.com) was scraped with BeautifulSoup.
Pandas was then used to convert the data obtained from the website into a data frame.
The tf-idf scheme was used to convert the text to vectors.
Finally, the sklearn package was used to build sentiment analysis model, using classification algorithms.
Having been trained with the reviews dataset, the model was used to classify test data as negative or positive positive review. Another model was built using vectors obtained with bag of words.
The results derived from the model built on the tf-idf scheme were compared with those obtained from a model built on bag of words.
