# Project Overview:
This Project is about predicting recommendation Rating based on Reviews data of customers.
# Description:
Each record in the dataset is a customer review which consists of the review title, text description and a rating (ranging from 1 - 5) for a product amongst other features.
I have converted this into a binary classification problem such that a customer recommends a product (label 1:good) if the rating is > 3 else they do not recommend the product (label 0:not good).
# Steps Followed:

# Step 1 : Some basic Pre-Processing
1. Merge all review text attributes (title, text description) into one attribute.
2. Convert the 5-star rating system into a binary recommendation rating of 1 or 0.
3.Removed all records without review text.

# Step 2 : 
1.Checked class imbalance.
2.Build train and test data

# Step 3 : Created some basic NLP count based features
1. Word Count: total number of words in the documents
2. Character Count: total number of characters in the documents
3. Average Word Density: average length of the words used in the documents
4. Puncutation Count: total number of punctuation marks in the documents
5. Upper Case Count: total number of upper count words in the documents
6. Title Word Count: total number of proper case (title) words in the documents

# Step 4 :Trained Logistic Regression Model and Evaluated The Model Performance
Here we saaw problem that our model was not learning anything and wa just classifying every product as label 1 that is good product

# Step 5 : Created some new features based on text sentiment to overcome previous issue
Reviews are pretty subjective, opinionated and people often express stong emotions, feelings. This makes it a classic case where the text documents are a good candidate for extracting sentiment as a feature.TextBlob is an excellent open-source library for performing NLP tasks with ease, including sentiment analysis. It also an a sentiment lexicon which it leverages to give both polarity and subjectivity scores.
1.The polarity score is a float within the range [-1.0,1.0].
2.The subjectivity is a float within the range [0.0, 1.0] where 0.0 is very objective and 1.0 is very subjective.

# Step 6 : Trained Logistic Regression Model on these new set of features and Evaluated Model Performance
Now our model is able to classify bad products also and is doing good but to make it a little more good we are gonna introduce some other features also to increase performance 

# Step 7 : Created Bag of Words based Features
## Text Pre-Processing:
1.Text Lowercasing
2.Removal of contractions
3.Removing unnecessary characters, numbers and symbols
4.Stemming
5.Stopword removal
## Separating structured features 
## created BOW based features
## combined both the features sets

# Step 8 : Final Model Training and Model Performance Evaluation
Now our model is doing much better than before two cases.
f1 score for bad reviews are 72% and good reviews are 92%.
Overall f1 score is 88%.




















