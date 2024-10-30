# Amazon Book Review - Dulguunzul

Here I have my code and data for performing sentiment analysis on Amazon Books. I have classified the review in "positive", 
"negative", and "neutral" sentiment using ULMFit model from FastAI library.

## About Dataset

This dataset includes:
- id: Unique ID for each book
- title: Title of the book
- price: Price of the book
- user_id: Id of user who rated the book
- profilename: Name of user who rated the book
- review/helpfulness: Helpfulness of the rating
- review/score: Rating the book from 0 to 5
- review/time: The time review was given
- review/summary: The summary of text review
- review/text: The full text of a review

## Process Overview
1. Data Preparation:
      - Dataset Upload: The dataset is uploaded as a CSV file containing Amazon Book reviews and associated ratings.
      - Sentiment Labeling: A function (label_sentiment) is applied to the ratings to categorize each review into three sentiment classes:
          - Positive (rating ≥ 4)
          - Negative (rating ≤ 2)
          - Neutral (rating = 3)
      - Data Splitting: The dataset is split into training and validation sets, with 80% for training and 20% for validation, using RandomSplitter.
2. Language Model Fine-Tuning:
A language model is pre-trained on general text data. To adapt it to the specific language patterns of Amazon Book reviews, it is further fine-tuned on the review text. This helps the model better understand the context, vocabulary, and structure of the reviews.
      - Fine-Tuning Steps: The model is trained on the reviews for four epochs with a learning rate of 1e−3. This fine-tuned language model is then saved as an encoder to be used in the next phase.
      - Text Classification Model: Using the fine-tuned language model as a starting point, a text classification model is created to predict the sentiment labels.
      - Progressive Fine-Tuning: A gradual unfreezing approach is applied, progressively training deeper layers of the model:
          - Initially, only the last layer is fine-tuned.
          - Subsequently, earlier layers are unfrozen and trained, gradually incorporating more of the model's layers until the entire model is fine-tuned.
This process optimizes the model's ability to differentiate sentiments in the reviews.

3. Model Evaluation:
      - A sample review is tested to demonstrate the model's prediction capabilities.
      - Confusion Matrix: The confusion matrix visually assesses the model's performance on the validation set, displaying how well it distinguishes between negative, neutral, and positive sentiments.
      - Classification Report: The classification report provides metrics such as precision, recall, and F1-score for each sentiment class, offering a quantitative evaluation of model accuracy.

## Results
The final model displays reasonable accuracy in classifying sentiments, as seen in the confusion matrix and classification report.
By leveraging fine-tuning and gradual unfreezing, the model demonstrates improved performance compared to training from scratch.
