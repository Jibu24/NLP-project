# NLP-project

The main objective of this project was to train a model to predict whether two questions asked in Quora are similar or not

## Project Flow
- Preprocessed texts to give optimal numeric representation
    - Remove Punctuation
    - Remove single characters
    - Remove stopwards
    - Lemmatize
    - Lowercase
- Used Tfidf (with max features =1000) and word2vec representation of texts as inputs for modelling
- Added the count of similar words between the two questions as a feature
- Used Gaussian Naive Bayes and Logistic Regression to predict class

## Results
- Using Tfidf vectorizer
    - Logistic Regression: 0.60 (f1score)
    - Guassian Naive Bayes: 0.58
- Using Word2vec 
    - Logistic Regression: 0.41
    - Guassian Naive Bayes: 0.43
## Limitations and Future Goals
- Large dataset, therefore numeric transformations and data preprocessing took a lot of time, with my kernel often stopping and restarting
    - Especially with word2vec transformations
- For Tfidf vectorizer I could not use more than 1000 max features before my kernel shutting down
    - I believe if more word features were allowed, better model performance woulda been achieved
- For the furture I would try to have equal distribution of classes because from the classification report I noted the model predicted the not-duplicate classes better due to larger sample size of that class
- Also would like to try better complex models like XGboost and even deep neural networks
