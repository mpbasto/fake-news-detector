# Fake News Classification Project 📰 
<img src="https://www.beknownforsomething.com/wp-content/uploads/2016/09/News.jpg" alt="Newspaper boy cartoon" title="Extra! Extra!" width="250" height="250" align='right'/> 


> *“In the age of information, ignorance is a choice.”* - Donald Miller


In this notebook, you will find an end-to-end binary classification model that detects **fake news** using sklearn.

### What is Fake News?

[Fake news](https://en.wikipedia.org/wiki/Fake_news#:~:text=Fake%20news%20is%20false%20or,reports%20in%20newspapers%20were%20common.) is false or misleading information presented as news. Fake news often has the aim of damaging the reputation of a person or entity, or making money through advertising revenue.

## Problem

Identifying whether a news deal is real or fake by its content.

> *I want to know if the news I'm reading are actually true.*

## Data

The dataset I’ll use for this project is called `news.csv` found in [DataFlair](https://data-flair.training/blogs/advanced-python-project-detecting-fake-news/). 

## Evaluation

Using sklearn, I will build a [`TfidfVectorizer`](https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.TfidfVectorizer.html) on the dataset. Then, I will initialize a [`PassiveAggressiveClassifier`](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.PassiveAggressiveClassifier.html) and fit the model. 

The `TfidfVectorizer` converts a collection of raw documents to a matrix of [TF-IDF](https://towardsdatascience.com/tf-idf-for-document-ranking-from-scratch-in-python-on-real-world-dataset-796d339a4089#:~:text=TF%2DIDF%20stands%20for%20%E2%80%9CTerm,Information%20Retrieval%20and%20Text%20Mining.) features, which is a word quantifier (determines a score for each word to mark its importance in a document).
* **TF (Term Frequency)** is the number of times a term occurs in a document.
* **IDF (Inverse Document Frequency)** is a measure of how much information the word provides, i.e., if it is common or rare across all documents.

The `PassiveAggressiveClassifier` is an [online learning](https://thecleverprogrammer.com/2021/02/10/passive-aggressive-classifier-in-machine-learning/) classification algorithm that remains passive for a correct classification outcome, and turns aggressive in the event of a miscalculation, update and adjustment.

In the end, the accuracy score and the confusion matrix tell us how well our model fares. A classification report will also be providing information of the precision and recall of our model for each class (precision, recall, f1-score, support, accuracy, macro average and weighted average).

## Features

There are a total of 6335 news articles in this dataset. There are also 4 attributes:
* `[id]` - identifies the news.
* `[title]` - the title of article and text, and the fourth column has labels denoting whether the news is REAL or FAKE.
* `[text]` - the text of article
* `[label]` - REAL and FAKE classes

## Conclusion
To be provided at the end of notebook.
