## Introduction

Welcome to the Fake News Detection Model repository! This project aims to develop a machine-learning model for detecting fake news in textual content. Social media platforms enable information to spread rapidly and globally. While this facilitates the dissemination of important news, it also amplifies the speed at which misinformation can circulate. In an era where information spreads rapidly through various channels, the ability to identify misinformation is essential. The end goal of this project is to create a predictive model that generalizes well to unseen data. This model will then be turned into an application that will allow people to test if news articles on social media are true or fake. 

### Motivation

Misinformation, especially in the form of fake news, has become a significant challenge in today's digital landscape.  This project was initiated to address the growing need for automated tools that can assist in distinguishing between credible and unreliable information sources.

### Key Features

- **Machine Learning Model:** The core of this project is a machine learning model trained on a large data set of short news articles to identify patterns and features associated with fake news.
    - **Logistic Regression:** The Logistic model worked very well when using the TFIDF vectorization. F1 score of .99 and accuracy of .99 as well when applied to the training data. 
- **Natural Language Processing (NLP):** Leveraging NLP techniques, the model analyzes the linguistic features of textual content to make informed predictions.
    - TF-IDF Vectorization: Term Frequency-Inverse Document-f=Frequency was used
      > Terms that are frequent in a specific document but rare across the entire corpus get higher TF-IDF scores, indicating their potential importance in describing the content of that document.
    - NLTK Stop words
      > Remove the words like "The" & "a" because they hold only small bits of information
    - NLTK Snowball stemmer 
- **Cross Vaildation**
      - cross-validation is used to test if our model will generalize
      - completely unseen data is used
      - results show that the original Logit model performed poorly

### Dataset

The model has been trained on a dataset from Kaggle [Kaggle](https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset) containing 40,00 both real and fake news articles.


### Next steps 

Cross-validation has shown us that the current method (Snowball, TFID, logit) is not generalizing well. There are a few things that can be done to improve performance. 
- try out embeddings(Word2vec, Doc2Vec, BERT)
- try a more complicated model 
