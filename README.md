# EMOJI PREDICTON SEMEVAL 2018 Task-2 

## Two Stage Classification

In the results of the model applied within the scope of the project, it was seen that emoji number 0 was very dominant in the predicted emojis. Therefore, two-stage classification is applied and in the first step, whether the input sentence belongs to emoji number 0 or any of the other 19 emojis; In the second step, if the sentence belongs to one of the other 19 emojis, it is decided which emoji it belongs to.

- [BERT Step-1](./BERT_STEP_1.ipynb): It is decided whether the sentence belongs to emoji number 0 or to one of the remaining 19 emojis.
- [BERT Step-2](./BERT_STEP_2.ipynb): If the sentence does not belong to emoji number 0, it is assigned to which of the remaining 19 emojis it belongs.

## BLSTM (With GloVe Word Embeddings)

