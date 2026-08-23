# Saudi News NanoGPT 🇸🇦

A character-level Transformer language model built and trained from scratch on Arabic news data using PyTorch.

## Overview

This project implements a small GPT-style language model for Arabic news text generation.

The model was trained from scratch using articles from the **SaudiNewsNet** dataset. The project covers the complete language-modeling pipeline, including Arabic text preprocessing, character-level tokenization, Transformer architecture implementation, training, validation, and text generation.

The goal of this project was to better understand how GPT-style Transformer models work internally rather than relying on a pre-trained language model.

## Dataset

The project uses the **SaudiNewsNet** dataset available through Hugging Face Datasets.

After preprocessing and filtering:

* **4,952 news articles**
* Approximately **8.8 million characters**
* **184 unique characters** in the vocabulary
* Articles formatted using:

```text
العنوان: [News Title]
الخبر: [News Content]
```

## Model Architecture

The language model was implemented from scratch using PyTorch and includes:

* Character-level tokenization
* Token embeddings
* Positional embeddings
* Multi-head causal self-attention
* Feed-forward neural networks
* Residual connections
* Layer normalization
* Dropout
* Autoregressive text generation

### Model Configuration

| Parameter          | Value |
| ------------------ | ----- |
| Embedding Size     | 128   |
| Attention Heads    | 4     |
| Transformer Blocks | 4     |
| Dropout            | 0.1   |
| Optimizer          | AdamW |

## Training

The dataset was divided into training and validation sets and the model was optimized using cross-entropy loss.

During training, the validation loss decreased from approximately **5.40 to 1.82**, demonstrating that the model successfully learned patterns in the Arabic news corpus.

## Example Generation

The model can generate Arabic news-style text from a topic prompt such as:

```text
العنوان: الذكاء الاصطناعي في السعودية
الخبر:
```

The model then continues generating text character by character based on patterns learned during training.

## Technologies

* Python
* PyTorch
* Hugging Face Datasets
* Transformer Architecture
* Natural Language Processing
* Google Colab

## What I Learned

Through this project, I gained hands-on experience with:

* Building a Transformer language model from scratch
* Implementing causal self-attention
* Multi-head attention mechanisms
* Character-level tokenization
* Preparing and cleaning Arabic NLP datasets
* Training and evaluating language models
* Autoregressive text generation
* Understanding the core architecture behind GPT-style models

## Limitations

This is a small educational language model trained at the character level with limited computational resources. Generated text may therefore contain grammatical or semantic inconsistencies.

Future improvements could include:

* Subword tokenization
* Larger training datasets
* Larger model architecture
* Improved text preprocessing
* More systematic evaluation
* Fine-tuning a pre-trained Arabic language model for comparison

## Notebook

The complete training and implementation pipeline is available in:

`saudi_news_nanogpt.ipynb`
