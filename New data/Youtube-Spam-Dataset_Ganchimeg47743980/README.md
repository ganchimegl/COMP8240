# YouTube Spam Detection
### Ganchimeg Lkhagvasuren - 47743980

## Overview

This project aims to develop a machine learning model capable of detecting spam comments on YouTube. With the vast amount of content on YouTube, spam detection is essential for maintaining a clean and safe platform. By leveraging the FastAI library for text classification and using sentiment analysis as additional input features, this project achieves a robust spam detection model to classify comments as "spam" or "not spam."

## Dataset

The dataset used in this project contains YouTube comments labeled as either spam or not spam, providing a binary classification task. It includes:

- **Text Content**: The raw comment text.
- **Spam Label**: A binary label (0 or 1), indicating whether a comment is spam (1) or not (0).

To download the dataset:
- [YouTube Spam Dataset](https://www.kaggle.com/datasets/ahsenwaheed/youtube-comments-spam-dataset) on Kaggle.
  
After downloading, place the dataset file in the project directory and ensure the file path in the code matches its location. Additionally, to enrich the dataset, sentiment-based features (polarity and subjectivity) are extracted from each comment using TextBlob, which helps capture the tone and intent of the comment.

## Project Approach

1. **Data Preprocessing**:
   - Load the dataset, rename columns for clarity, and split it into training and testing sets.

2. **Feature Engineering**:
   - Sentiment analysis features—**polarity** (positivity/negativity) and **subjectivity** (objectivity/subjectivity)—are generated for each comment. These sentiment features provide additional context that can aid in distinguishing spam from non-spam text.

3. **Data Preparation for Model**:
   - A `TextDataLoader` is created with FastAI, incorporating sentiment features as continuous variables to improve model performance.

4. **Model Training**:
   - The text classifier is trained using FastAI’s `AWD_LSTM` model, which is fine-tuned on the spam detection task.

5. **Model Evaluation**:
   - The trained model is evaluated on the test data, generating classification metrics to assess its performance on identifying spam comments.

## Project Structure

- **ULFIT2.ipynb**: Main Jupyter notebook with code and analysis for Youtube Spam Detection.
- **README.md**: Project overview and instructions.
  
## Setup and Dependencies

This project uses the following main dependencies:
- Python 3.7+
- [fastai](https://docs.fast.ai/) (version 2.0 or above)
- PyTorch (compatible with fastai)

