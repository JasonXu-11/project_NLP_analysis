#  ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & NLP Jiacheng Xu

### Introduction

In this project, we'll use  webscraping, APIs, and Natural Language Processing to train classifiers on which subreddit posts belong to.

### Submission
* Get_url.ipynb
* EDA.ipynb
* NLP.ipynb
* Sentiment.ipynb
* README.md
* Presentation Project 3.pdf



### Use API for webscraping
https://api.pushshift.io/reddit/search/submission

Instead of using comment, we will use **submission** to scrape some basic information of posts.

**pushshift** is a tool we can use to access reddit's API.

### Subreddit
1. CryptoCurrency
2. StockMarket

**CryptoCurrency** has 3.1 million users and 26.9K of them are active. It is created in 2013.

**StockMarket** has 1.6 million users and 2.8K of them are active. It is created in 2008

### Webscraping
* 1000 posts for each subreddit
* 83 columns for CryptoCurrency, 81 columns for StockMarket
* Save in two files and ready for EDA

### EDA
- **selftext** columns contains the description of a post.
  - 427 NaN in StockMarket selftext column, 441 NaN in CryptoCurrency selftext.
- EDA on columns **['title','id','author','subreddit','score']**.
- Calculate **title length** and **number of words**.
- Visualize title length
- Visualize score v.s number of words
- Discover author's post habit
- EDA on words using
  - Most frequently used words

### NLP Classification
- Model Selection
  - **Random forest**
  - **Extra trees**
  - **SVM (kernal)**
- Train-test-split
- Pipeline and GridSearch
- Analyze with confusion matrix and Classification report

### Sentiment Analysis
- Tokenization
  - RegexpTokenizer
- Sentiment Analysis
  - Valder sentiment analyzer
  - Polar score

### Conclusion
1. All my classification models are overpredicting.
2. Random Forest and Extra Trees are predicting the most accurately with high variance.
3. SVMs is predicting slightly worse but has a lower variance.
4. Random Forest and Extra Trees both have high precision score for predict Cryptocurrency.
5. SVMs doing well for predicting both subreddits.
6. Both subreddits' text have very similar sentiment result.
