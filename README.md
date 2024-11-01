# COMP8240: ULMFiT Replication and Adaptation (Novel Project)
## October 2024 | Group D

## Overview
This project replicates the Universal Language Model Fine-tuning (ULMFiT) approach, originally proposed by Howard and Ruder (2018), to evaluate its effectiveness on a variety of text classification tasks. ULMFiT, known for its simplicity and adaptability, utilizes transfer learning for Natural Language Processing (NLP), employing techniques like discriminative fine-tuning, gradual unfreezing, and slanted triangular learning rates. The project aims to validate the original model’s results on the IMDb Large Movie Review Dataset and further tests ULMFiT’s versatility across additional datasets, such as Twitter Airline Sentiment, Kindle Reviews, YouTube Spam Detection, and Amazon Product Reviews.

## Project Goals
1. Replicate ULMFiT’s reported 4.6% error rate on the IMDb dataset to confirm its effectiveness on sentiment analysis.
2. Adapt the ULMFiT model to new datasets, evaluating its performance and robustness across varied text types.
3. Analyze the role of feature engineering and preprocessing techniques, such as polarity and subjectivity, in improving model accuracy for noisy, real-world data.

## Datasets Used
### Replication
1. IMDb Large Movie Review Dataset: Used to replicate the original ULMFiT results on sentiment classification.

### New datasets
2. Twitter US Airline Sentiment: Sentiment analysis on tweets directed at major US airlines.
3. Kindle Reviews: Sentiment classification on user reviews from Amazon’s Kindle platform.
4. YouTube Spam Dataset: Binary classification to detect spam and non-spam comments.
5. Amazon Product Reviews: Sentiment analysis on a subset of Amazon reviews.

## Model and Techniques
ULMFiT is a three-stage NLP transfer learning approach:

- General-domain Language Model Pretraining: A language model pretrained on a large corpus establishes foundational language patterns.
- Target Task Language Model Fine-Tuning: The model is fine-tuned on task-specific datasets (e.g., IMDb, Twitter).
- Classifier Fine-Tuning: The final classifier is trained with techniques like gradual unfreezing and discriminative fine-tuning.

Additional preprocessing techniques, including polarity and subjectivity analysis, were used to capture nuanced text features that aid classification accuracy.

## Results Summary
1. IMDb Dataset: Achieved a 5.48% error rate, closely aligning with the original 4.6% rate reported by Howard and Ruder.
2. Extended Datasets: ULMFiT performed effectively across varied text sources with accuracy rates between 70% and 93%, demonstrating adaptability.

## Usage
1. Clone the repository:

```bash
1. Clone the repository
git clone https://github.com/username/repo-name
cd repo-name
```

2. Install dependencies
```bash
pip install -r requirements.txt
```
3. Run experiments: Each dataset folder contains specific notebooks and instructions for replicating experiments.


## Contributors
1. Ganchimeg Lkhagvasuren (47743980)
2. Parinya Sodsai - 47817283
3. Shrishti Lulla - 47686529
4. Dulguunzul Battsengel - 47634553

## References
Howard, J., & Ruder, S. (2018). Universal language model fine-tuning for text classification. arXiv preprint arXiv:1801.06146.
