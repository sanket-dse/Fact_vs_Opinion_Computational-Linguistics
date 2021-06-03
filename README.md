# Fact_vs_Opinion_Computational-Linguistics
A project where we try to build Machine Learning models to differentiate factual articles from opinion pieces 

## Introduction
In the era of the world wide web, like most things, journalism has also seen a revolutionary
change. Online media has altered the nature, distribution and representation of journalism.
While it has helped boost accessibility, transparency and involvement of local communities, it
has also posed problems about authenticity and manipulation of facts. Therefore, it is important
not only to segregate fake news, but also opinionated news from fact-based news. This is not
just a question of improving the quality of news and narrowing down our search for
manipulative, possibly harmful news articles, but also to categorize different types of journalism
into objective and subjective.
A fact is a statement that can be proven either right or wrong. On the other hand, an opinion is
an expression of a group or individual’s feelings. Opinionated news may be based on facts and
factual news may contain opinions too. So, it is not always easy to have a clear distinction
between the two. Our humanly biases may also come into play.
In this project, we have taken datasets of fact-based and opinion-based news articles, tried to
analyse the similarities and differences between them, and built various models, training and
testing them, and analysing their accuracies. This is a first step towards creating a fact vs
opinion based news-classifier.

## Linguistic Theories and ML models used
### Assumptions/Theories:
1. Any article falls to either the opinion-based or the fact-based category.
2. Articles from certain categories were all assumed to be fact-based, as described
in the Datasets section below.
3. It is assumed that the PoS tagger used tagged the training set with 100%
accuracy.
### Models
We tried out quite a few conventional Machine learning models to classify the articles -
* *Multinomial Naive Bayes Classifier*

Naive Bayes is based on Bayes’ theorem, where the adjective Naïve says that
features in the dataset are mutually independent. Occurrence of one feature
does not affect the probability of occurrence of the other feature.
* *Random Forest Classifier*

 Random Forest is an ensemble method, meaning that a random forest model
is made up of a large number of small decision trees, called estimators, which
each produce their own predictions. The random forest model combines the
predictions of the estimators to produce a more accurate prediction.
* *K Nearest Neighbors Classifier*

 KNN algorithm is used to classify by finding the K nearest matches in training
data and then using the label of closest matches to pretict. Traditionally,
distance such as euclidean is used to find the closest match.
* *Support Vector Classifier*

 Support Vector Classifier is a supervised machine learning algorithm where
each data item is plotted as a point in n-dimensional space (where n is number
of features) with the value of each feature being the value of a particular
coordinate. Then, classification is performed by finding the hyper-plane that
differentiates the two classes very well.

## Datasets
The datasets used were taken from two UK based news publishing houses - ‘BBC’ and
‘The Guardian’. The fact based articles were ‘scraped’ from different sections like politics,
technology, sports, entertainment and business on the BBC News website. The opinionated
articles were extracted from the ‘Opinion’ section on The Guardian website. This consisted of
editorials and opinion pieces from columnists.

For the final litmus test, we compiled a rather small dataset of 10 articles (due to time
constraints) from ‘The Hindustan Times’ and the articles were specific to events revolving
around India. Opinionated articles were compiled from the “Opinion” section and the fact based
articles from sections under ‘cities’, ‘tech’, ‘education’ and ‘cricket’

## Files Involved 

1. *Comp_ling_Classification_models1.ipynb* - A python notebook outlining the classification of non POS tagged dataset
2. *Comp_ling_Classification_models1.ipynb* - A python notebook outlining the classification of POS tagged dataset
3. *Comparision_Analysis.html* - The html version of python notebook containing the preliminary data exploration of the datasets.
4. *WebScrapingGuardian.ipynb* - The python notebook to extract the opinion pieces from the 'Guardian' website.
5. All other are the *datasets* involved. They would be self explanatory.

## Limitations and Scope of this Project
1. The analysis may be imprecise owing to the source of the articles, the
size and nature of the dataset. 
2. The training set consisted of news articles pertaining to the UK and the
US. This could have affected the machine learning models’ accuracies
while classifying Indian centric news articles. Expanding the final testing
dataset could have enabled us to find robust conclusions regarding the
generalizability of the models.
3. The possible solutions could be incorporating all kinds of regional news
articles in the training set or finding out further linguistic differences
between factual sentences and sentences expressing opinion viz.
*sentence level classification of the articles.*
4. Models’ accuracies and generalization capabilities could have been
further increased if we could have removed stop words from the POS
tagged news articles.
