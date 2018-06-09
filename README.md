# fake_or_real_news_classifier
#### This project is studying on applying machine learning algorithm to figure out whether a piece of news is real or fake.
* [Wei_Lan_NLPproject.ipynb](https://github.com/Lanwei02/fake_or_real_news_classifier/blob/master/Wei_Lan_NLPproject.ipynb): 
In this file, I vectorized the full text using countVectorizer and tfidfVectorizer separately as the input features and uesed naive bayes algorithm to build the calssifier. To improve the accuracy of the model, I have tried two types of stop word  —— one is the default stop word of scikit-learn package and the other one is scrapped from [Onix](http://www.lextek.com/manuals/onix/stopwords1.html) —— and tried 'gram_range' with different values. Also, I used Grid Search function to apply cross validation to find the best parameter for naive bayes classifier. 
The outcomes showed that the stop words downloaded from Onix is more suitable to the data set used here. Also, I have tried 
