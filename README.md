# fake_or_real_news_classifier
#### This project is studying on applying machine learning algorithm to figure out whether a piece of news is real or fake.
* [Wei_Lan_NLPproject.ipynb](https://github.com/Lanwei02/fake_or_real_news_classifier/blob/master/Wei_Lan_NLPproject.ipynb): 

In this file, I vectorized the full text using countVectorizer and tfidfVectorizer separately to made two groups of input features and built classifiers with naive bayes for them individually.

To improve the accuracy of the models, I have tried two types of stop word  —— one is the default stop word of the sci-kit-learn package, and the other one is scrapped from [Onix](http://www.lextek.com/manuals/onix/stopwords1.html) —— and tried 'gram_range' with different values. Also, I used Grid Search function to apply cross-validation to find the best parameter for naive bayes classifier. 

The outcomes showed that both of the two classifiers performed better when using the downloaded stop words and (3,3) of the 'ngram_range' and the classifier with a tfidf vectorizer worked better(accuracy is 0.925).
