# Twitter US Airline Sentiment Analysis

This repository contains code and data for performing sentiment analysis on tweets directed at major U.S. airlines. Using the ULMFiT (Universal Language Model Fine-tuning) approach, the model is fine-tuned on this dataset to classify tweets as **positive**, **neutral**, or **negative**.

---

## Repository Contents

1. **Code**: The Python code provided in `ulfit_newdata_parinya.py` is used for:
   - Data preprocessing and tokenization
   - Fine-tuning a language model on airline-related tweets
   - Training a sentiment classifier
   - Generating and plotting a confusion matrix to evaluate the model's performance

2. **Dataset**: The `Tweets.csv` file contains the Twitter US Airline Sentiment dataset, with each tweet labeled with sentiment (positive, neutral, or negative) and other metadata.
   - **Source**: [Twitter US Airline Sentiment Dataset on Kaggle](https://www.kaggle.com/datasets/crowdflower/twitter-airline-sentiment/data)

---

## Dataset Description

The `Tweets.csv` file contains tweets directed at major U.S. airlines, capturing traveler sentiment from February 2015. This dataset includes:
- **tweet_id**: Unique ID for each tweet
- **text**: Original tweet text
- **airline_sentiment**: Sentiment label for each tweet (positive, neutral, negative)

## Requirements

To run this code, the following Python libraries are required:
- `fastai`
- `pandas`
- `spacy`
- `seaborn`
- `matplotlib`
- `scikit-learn`
  
You can install these using:
```bash
pip install fastai pandas spacy seaborn matplotlib scikit-learn
```

---

## Instructions
1. **Data Preprocessing**: The code preprocesses the text in the dataset by:
- Converting text to lowercase
- Removing punctuation

2. **Model Training**
The model training is divided into two main steps:

- Language Model Training: Fine-tune a language model on the airline tweet dataset to adapt to the vocabulary and style of tweets.
Sentiment Classification: Train a classifier using the pre-trained encoder from the language model to predict the sentiment of each tweet.

3. **Model Evaluation**
The model's performance is evaluated on a validation set, and a confusion matrix is generated to visualize how well the model distinguishes between the three sentiment classes.

Usage
To run the code:

Ensure `Tweets.csv` is in the same directory as the script.
Run the following command in the terminal:
bash
```bash
python ulfit_newdata_parinya.py
```
This script will preprocess the data, train the language model and classifier, and then output the model’s validation accuracy and loss. Additionally, it will display a confusion matrix to assess classification performance.

**Results**

The model achieves a validation accuracy of approximately 81%, with some difficulty in predicting the neutral class accurately. The confusion matrix provides a detailed view of the classification results for each sentiment class.

---
