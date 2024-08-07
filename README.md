# Emoji Prediction - SemEval 2018 Task-2

Our **computer project**, __"Emoji Prediction from Text as a Sentiment Analysis Method"__, involves predicting emotion from text through semantic analysis. The aim of our project is to classify data with various classification algorithms and predict emojis on unclassified data. Learn more about [competition](https://competitions.codalab.org/competitions/17344).

The training file can be downloaded from the provided [link](https://codalab.lisn.upsaclay.fr/competitions/8121) for the dataset.



## Normalization

- Punctuation marks, stopwords, URL characters, HTML characters, and excess spaces have been removed.
- All data has been converted to lowercase.
- The '@' and '#' signs in tweets have been removed.
- Extra letters in words with letter repetition have been deleted.

These processes aim to organize and standardize the data.

## Two Stage Classification with BERT

The results of the model revealed that emoji number 0 was very dominant in the predicted emojis. Therefore, a two-stage classification is applied:
1. In the first step, it determines whether the input sentence belongs to emoji number 0 or any of the other 19 emojis.
2. In the second step, if the sentence belongs to one of the other 19 emojis, it decides which emoji it belongs to.

- [BERT Step-1](./BERT_STEP_1.ipynb): Determines whether the sentence belongs to emoji number 0 or to one of the remaining 19 emojis.
- [BERT Step-2](./BERT_STEP_2.ipynb): If the sentence does not belong to emoji number 0, it assigns it to one of the remaining 19 emojis.

## BLSTM (With GloVe Word Embeddings)

### What is GloVe Word Embeddings?

GloVe is a distributional word embedding method used for word representations. In our models, the "glove.twitter.27B.200d" model is utilized. This pre-trained version of the GloVe model is trained on social media data, specifically 27 billion tweets, and represents each word through a 200-dimensional vector.

- Learn more about [Stanford GloVe Model](https://nlp.stanford.edu/projects/glove/)
## Accuracy Rates

| Model        | Accuracy Rate                 |
|------------------|----------------------------|
| Two Stage Classification with BERT     | 27% |
| BLSTM (With GloVe Embeddings)    | 29%|

More than 20 models were tested within the scope of the project. The two most successful models have been added to the Github repository. You can review the [report](Report.pdf) and [article](Article.pdf) files for information on other tried models.

## DEMO

After running the entire code, pressing the button that appears on the screen selects a random tweet from the test dataset and predicts an emoji for it. It then displays both the correct emoji and the predicted emoji on the screen.
