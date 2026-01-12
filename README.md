# Fine-tuning BERT for Emotion Classification (GoEmotions)

## 👥 Team Information
**Course**: Deep Learning  
**Institution**: Telkom University  

| Name | NIM |
|------|-----|
| Alvito Kiflan Hawari | 1103220235 |
| Nafal Rifky Atsilah Maulana | 1103223106 |

---

## 🎯 Purpose
This repository contains the implementation of a **multi-class emotion classification** project using **BERT**.

The objective of this project is to fine-tune a pre-trained **BERT (Bidirectional Encoder Representations from Transformers)** model on the **GoEmotions** dataset to classify emotions expressed in short text sentences.

---

## 🔍 Project Overview

### The Task: Emotion Classification
Emotion classification is a **natural language understanding task** where the goal is to identify the emotional content expressed in text.  
Each input sentence is mapped to one of several predefined emotion categories.

### The Dataset: GoEmotions
**GoEmotions** is a large-scale, human-annotated dataset of Reddit comments labeled with emotions.

- **Input**: Short text (sentence or comment)
- **Output**: One emotion label
- **Emotion Classes**: 28 fine-grained emotions (e.g., joy, sadness, anger, fear, surprise, etc.)
- **Label Type**: Single-label classification (one dominant emotion per text)

---

## 🤖 Model Description

### The Model: BERT-base
- **Base Model**: `bert-base-uncased`
- **Architecture**: Encoder-only Transformer
- **Pre-training Objectives**:
  - Masked Language Modeling (MLM)
  - Next Sentence Prediction (NSP)

### Fine-tuning Strategy
- A classification head is added on top of BERT’s `[CLS]` token
- The entire model is fine-tuned end-to-end for emotion classification
- Cross-entropy loss is used for optimization

---

## 📊 Technical Approach

### Model Configuration
- **Base Model**: `bert-base-uncased`
- **Tokenizer**: `BertTokenizerFast`
- **Framework**: PyTorch & Hugging Face Transformers
- **Task Type**: Multi-class text classification

### Training Configuration
- **Batch Size**: 16
- **Learning Rate**: 2e-5
- **Epochs**: 3
- **Optimizer**: AdamW
- **Loss Function**: Cross-Entropy Loss
- **Evaluation Metrics**:
  - Accuracy
  - Precision
  - Recall
  - F1-score

---

## 📁 Repository Structure
finetuning-bert-goemotions/
│
├── notebooks/
│ └── Finetuning-Bert-GoEmotions.ipynb # Main Jupyter Notebook
│
├── models/
│ └── bert-goemotions.pt # Saved fine-tuned model
│
└── README.md # Project documentation
