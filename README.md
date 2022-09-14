# Kaggle: [Natural Language Processing with Disaster Tweets](https://www.kaggle.com/competitions/nlp-getting-started/)


This task is a binary classification problem, identifying whether tweets are referring to genuine disasters. I fine-tuned a pretrained [RoBERTa](https://arxiv.org/abs/1907.11692) model using PyTorch. The [original model](https://github.com/VinAIResearch/BERTweet) was trained on English Tweets. Since unnormalized location and keyword fields were supplied as well, I combined the transformer output on all of these fields before the final classification layer.

### Results

The Kaggle test set F1 score was 0.836. Below is the performance of the model on a held out development test set of 1,739 tweets.

|   | Precision | Recall | F1   | Support | Accuracy |
|---|-----------|--------|------|---------| -------- |
| 0 | 0.84      | 0.91   | 0.87 | 1029    |          |
| 1 | 0.85      | 0.75   | 0.80 | 710     |          |
|   |           |        |      |         | 0.85     |

![Confusion Matrix](results/confusion_matrix.svg)
![ROC Curve](results/roc_curve.svg)