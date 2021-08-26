# NPL-Assignment-Sentiment_Analysis_Amazon_Reviews

Sentiment analysis on amazon product review dataset at https://nijianmo.github.io/amazon/index.html.

## Pre-Processing

The review text is pre-processed and cleaned using the following pipeline,
- Remove HTML code.
- Make everything lower case.
- Expand contractions.
- Remove numbers.
- Remove stop words.
- Remove punctuation symbols.
- Tokenize sentences.
- Lemmatize sentences.

## Corpus

After pre-processing, the corpus size is `1071723` words and the vocabulary size is `31721` words.

Some words in the corpus in order of frequency are,

|Word|Frequency|
|-|-|
|book|31936|
|read|18290|
|one|10860|
|story|10508|
|love|7478|
|character|7322|
|like|6995|
|great|6808|

## Sentiment analysis

Sentiment analysis was done using multiple methods.

The results for the methods are as follows,

|Model|Vectorizer|Accuracy|F1 Score|
|-|-|-|-|
|Naive Bayes (MultinomialNB)|Count Vectorizer|87.71%|93.04%|
|Naive Bayes (MultinomialNB)|TF-IDF Vectorizer|85.80%|92.36%|
|Naive Bayes (MultinomialNB)|average_word_embeddings_glove.840B.300d|85.80%|92.36%|
|DecisionTreeClassifier|Count Vectorizer|82.89%|90.03%|
|DecisionTreeClassifier|TF-IDF Vectorizer|83.47%|90.48%|
|DecisionTreeClassifier|average_word_embeddings_glove.840B.300d|80.00%|88.27%|
|LogisticRegression|Count Vectorizer|88.49%|93.49%|
|LogisticRegression|TF-IDF Vectorizer|88.21%|93.51%|
|LogisticRegression|average_word_embeddings_glove.840B.300d|87.93%|93.26%|

