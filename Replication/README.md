# COMP8240

# Replicating ULMFiT for Text Classification on IMDb Dataset

This project replicates the Universal Language Model Fine-tuning (ULMFiT) approach for text classification, specifically targeting binary sentiment classification on the IMDb dataset. This notebook aims to achieve results similar to those reported by McCann et al. (2017) with an approximate error rate of 4.6%.

## Project Overview

The primary goal of this project is to:
1. Fine-tune a language model on the IMDb dataset to capture the language characteristics of movie reviews.
2. Use the fine-tuned language model to initialize a text classifier.
3. Train the classifier on the IMDb dataset to distinguish between positive and negative reviews.

The final error rate achieved in this replication was approximately 5.48%, which is close to the target 4.6% reported in the original paper. Small discrepancies may be due to differences in model parameters, random initialization, or dataset splits.

## Dataset

The IMDb Large Movie Review Dataset is used for binary sentiment classification. It contains:
- 25,000 highly polar movie reviews for training.
- 25,000 movie reviews for testing.
- Additional unlabeled data for language model fine-tuning.

Due to its size, the dataset cannot be included directly in this repository. Please download it from the official source:

[Large Movie Review Dataset v1.0 (IMDb)](https://ai.stanford.edu/~amaas/data/sentiment/)

### Instructions to Download the Dataset

1. Visit the [IMDb dataset page](https://ai.stanford.edu/~amaas/data/sentiment/).
2. Download and extract the dataset to your preferred directory.
3. Update the dataset path in the code as needed.

Alternatively, the code in this repository uses the `fastai` library’s `untar_data` function to automatically download and prepare the IMDb dataset if an internet connection is available.

## Project Structure

- **ULFIT2.ipynb**: The main Jupyter notebook for replicating the ULMFiT process, including both language model fine-tuning and text classification.
- **README.md**: Project overview and instructions.
  
## Setup and Dependencies

This project uses the following main dependencies:
- Python 3.7+
- [fastai](https://docs.fast.ai/) (version 2.0 or above)
- PyTorch (compatible with fastai)
