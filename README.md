# Punctuation Restoration with Fine-Tuned SlovakBERT

This project provides a Python-based implementation for fine-tuning a pre-trained SlovakBERT model to restore punctuation in text. It utilizes the Hugging Face `transformers` library and PyTorch for natural language processing tasks such as tokenization, model training, and prediction.

## Table of Contents

- [Library Setup](#library-setup)
- [Text Preprocessing](#text-preprocessing)
- [Fine-Tuning](#fine-tuning)
- [Punctuation Restoration](#punctuation-restoration)
- [Interactive Interface](#interactive-interface)
- [Data Handling](#data-handling)
- [Practical Example](#practical-example)
- [Requirements](#requirements)
- [Installation](#installation)

## Library Setup

The script loads the pre-trained **SlovakBERT** model and tokenizer, designed for **Masked Language Modeling (MLM)**, to predict and restore missing punctuation in the text.

## Text Preprocessing

The preprocessing step involves:

- Masking punctuation marks in the text.
- Converting the text into a format that can be used for model training.

A function is provided to preprocess the input text, ensuring it is ready for the fine-tuning process.

## Fine-Tuning

Fine-tuning is performed by adjusting the model's weights to predict masked punctuation marks. The following steps are taken:

1. **Tokenization**: Text is tokenized into token IDs using the SlovakBERT tokenizer.
2. **Dataset Creation**: A custom PyTorch dataset is created for masked language modeling.
3. **Training**: The model is trained using masked tokens, a loss function, and an optimizer. Training hyperparameters can be configured for better performance.

## Punctuation Restoration

Once the model is fine-tuned, it can be used to restore punctuation in text. The restoration process involves:

- Iteratively masking tokens.
- Using the fine-tuned model to predict the correct punctuation.
- Replacing the masked tokens with predicted punctuation marks.

## Interactive Interface

An interactive command-line interface is provided to let users:

1. Train the model on custom text data.
2. Correct punctuation in user-provided text input.

## Data Handling

The script supports reading **JSON** data files, where:

- Punctuation positions are marked.
- The dataset is processed to identify the masked punctuation marks for training.

## Practical Example

A practical example is included, where:

1. The model is fine-tuned on Slovak text.
2. The punctuation restoration function is used to correct punctuation in user-inputted text.

## Requirements

- Python 3.6 or higher
- PyTorch 1.6+
- Hugging Face Transformers 4.0+
- NLTK 3.5+

## Installation

Clone this repository and install dependencies:

```bash
git clone https://github.com/yourusername/punctuation-restoration.git
cd punctuation-restoration
pip install -r requirements.txt
