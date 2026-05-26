# Sentiment-Analysis-of-Free-Meal-Program-in-Indonesia

This repository contains a comparative sentiment analysis project on Indonesian YouTube comments related to the Free Nutritious Meal Program (Makan Bergizi Gratis / MBG) using several deep learning architectures:
- BiLSTM
- BiLSTM + Attention
- BiGRU
- BiGRU + Attention
- IndoBERT

The project evaluates the effectiveness of recurrent neural networks and transformer-based models for Indonesian sentiment classification tasks.

## Project Overview

Social media platforms contain large amounts of public opinion regarding government policies and social programs. This project focuses on analyzing sentiments toward the MBG program using Indonesian-language YouTube comments.

The models classify comments into three sentiment categories:
- Neutral
- Positive
- Negative

The project also includes:
- Attention mechanism analysis
- Ablation study (with vs without attention)
- Cross-validation
- Confusion matrix evaluation
- Direct inference testing

## Installation

### 1. Clone Repository

```bash
git clone https://github.com/yourusername/mbg-sentiment-analysis.git
cd mbg-sentiment-analysis
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

Or manually install:

```bash
pip install torch transformers datasets scikit-learn pandas numpy matplotlib seaborn tqdm tensorboard
```

## IndoBERT Model (Not Included in Repository)

The IndoBERT model is NOT included inside this repository because the pretrained transformer weights are very large. Instead, the model will automatically be downloaded from Hugging Face when running the notebook.

```bash
from transformers import AutoModelForSequenceClassification

model_bert = AutoModelForSequenceClassification.from_pretrained(
    "indolem/indobert-base-uncased",
    num_labels=3
)
```

## Author

Feliks Sung
