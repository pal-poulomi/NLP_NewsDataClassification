# NLP_NewsDataClassification
NLP project for categorizing news articles using Doc2Vec algorithm
## Multiclass Text Classification: News article data
- This NLP project is a supervised learning problem where we try to predict the category of a news article. Since each article belongs to exactly one of the 5 categories used here, it is a multiclass classification problem.

## Data Collection
- I used a data set named BBC news data
- Read in the data as a pandas dataframe
- The data set has 5 categories of data (business, sport, tech, politics and entertainment) and has more than 2000 articles with 2 features (text data and  category/label)
## Data pre-processing and cleaning
- Dropping duplicate rows
- Plotting the count of articles in each category and the data was not imbalanced
- Counting and plotting the number of words in each article
- Convert text into lowercase, remove extra spaces, tags, punctuations, digit and special characters from the text.
- I used WordCloud to visualize the most frequent words present in each category
- Further cleaning of text, that is, stop word removal and tokenization
- Finally, label encoding, to convert the target labels (text) to numeric. I saved the preprocessed data in a csv file.
## Feature extraction, training and testing, model building
- Split the cleaned text into training and testing sets
- Performing feature extraction using Tf-Idf (term frequency inverse document frequency)
## Model building: 
- I used supervised learning algorithms such as Random Forest Classifier, Logistic regression, KNN, Decision tree, Naive Bayes and SVM, of these Logistic regression gave the best accuracy
## Hyper parameter tuning
- I used hyperparameter tuning on Logictic regression algorithm, and that slightly increased the accuracy
- Using Doc2Vec algorithm instead of Tf-Idf
- Using the cleaned text csv file, converting training and testing data into the Gensim format
- Initializing the Doc2Vec model and training it for a few epochs
- Getting the vector representations of the train and test sets
- Finally, using Logistic regression model again with the new train and test vectors and achieving an increase of 1% in accuracy (95%)
