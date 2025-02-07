# N-Gram Text Generation Model

## Overview

This repository contains a Jupyter Notebook implementing an N-Gram Language Model for text generation. The model is trained on Shakespearean text and generates synthetic text based on learned probabilities of word sequences.

## Contents

- **ngram_text_gen.ipynb:** Jupyter Notebook containing code and explanations.

- **README.md:** This file, providing an overview of the project.

- **shakespeare.txt:** Training dataset containing a collection of Shakespeare’s works.

## Requirements

To run this notebook, install the following dependencies:

pip install numpy, pandas, nltk

## Dataset

The dataset consists of Shakespearean sonnets and plays. It is preprocessed to extract sentences for training the language model.

### Preprocessing Steps:

- **Reading the Data:** The text file is loaded and split into individual sentences.

- **Tokenization:** Sentences are tokenized into words while preserving punctuation.

- **Vocabulary Creation:** A vocabulary of unique words is constructed for further processing.

- **Stopword Removal:** Common words (like "the", "is", "and") are removed to focus on meaningful tokens.

## Key Features

1. Understanding N-Gram Models

- **Bigram Model:** Considers only the previous word when predicting the next word.

- **Trigram Model:** Expands the context to two previous words.

- **Higher-order N-grams:** Can be extended to incorporate more words in context.

2. Model Implementation

- The NGramModel class is implemented to:

  - **Tokenize text:** Break sentences into words, handling punctuation and special characters.

  - **Generate n-grams:** Create sequences of word pairs (bigrams), triplets (trigrams), or higher-order n-grams.

  - **Compute n-gram probabilities:** Estimate likelihoods of word sequences occurring together.

  - **Predict next words:** Given a context, predict the next most probable word using stored n-gram probabilities.

3. Likelihood Estimation

- Uses Maximum Likelihood Estimation (MLE) to compute probabilities.

- Implements Laplace Smoothing to handle unseen n-grams and prevent zero probabilities.

- Stores frequency distributions of word sequences.

4. Text Generation

- Generates text using learned probabilities from the trained n-gram model.

- Uses randomized sampling for diversity in predictions.

- Accepts user-defined prompts to influence text output.

- Ensures grammatically coherent sentences by leveraging higher-order n-grams.

5. Evaluation

- Computes log-likelihood scores for evaluating generated text.

- Compares bigram vs. trigram models to analyze text fluency.

- **Performance Metrics:**

  - Higher log-likelihood scores indicate better model performance.

  - Bigrams tend to generate simpler patterns, while trigrams yield more structured text.


## Results Summary

- Bigram models capture basic word patterns but may lack coherence.

- Trigram models generate more natural text due to larger context windows.

- Log-likelihood scores indicate that longer n-grams improve prediction accuracy.

- Text completion experiments show that n-gram models can produce structured, Shakespeare-like text.

## Future Improvements

- Implement backoff strategies to handle unseen word sequences better.

- Experiment with higher-order n-grams for better fluency.

- Integrate neural language models (e.g., RNNs, Transformers) for comparison.

