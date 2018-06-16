# fake_or_real_news_classifier
#### This project is studying on applying machine learning algorithm to figure out whether a piece of news is real or fake.
* [Wei_Lan_NLPproject.ipynb](https://github.com/Lanwei02/fake_or_real_news_classifier/blob/master/Wei_Lan_NLPproject.ipynb): 

In this file, I vectorized the full text of the fake_or_real_news.csv using countVectorizer and tfidfVectorizer separately to made two groups of input features and built classifiers with naive bayes for them individually.

To improve the accuracy of the models, I have tried two types of stop word  —— one is the default stop word of the sci-kit-learn package, and the other one is scrapped from [Onix](http://www.lextek.com/manuals/onix/stopwords1.html) —— and tried 'gram_range' with different values. Also, I used Grid Search function to apply cross-validation to find the best parameter for naive bayes classifier. 

The outcomes showed that both of the two classifiers performed better when using the downloaded stop words and (3,3) of the 'ngram_range' and the classifier with a tfidf vectorizer worked better(accuracy is 0.925).

* [FakeRealNews.ipynb](https://github.com/Lanwei02/fake_or_real_news_classifier/blob/master/FakeRealNews.ipynb):

This is the second version of the project which is done after I read some more materials about sentiment analysis. Also, I found that the dataset has some duplicate news which I did not see last time and I removed them this time. 

In this version, I used the pipeline to combine feature preprocessing method with Naive Bayes so that I can tune more hyperparameter combinations. I also tried news' title as the input features, but the accuracy is obviously lower than using news' text as input features. The best classifier I got in this step is using TfidfVectorizer(lowercase = False, min_df = 3, ngram_range = (1, 3)) as input features preprocessing method and Naive Bayes with alpha equal to 0.1 as classification algorithm. The testing accuracy I have got is 92.33%.

Besides, I used the Tfidf Vectorizer with the best parameters as my preprocessing method and tried Logistic Regression and Linear Support Vector Machine, which are two normally used algorithms during sentiment analysis. After fine tuning the parameters, the accuracy reaches 94.61% with logistic regression and 94.61% with linear SVC.
