# 🚀 Transformer-Based Next Word Prediction (From Scratch)

## 📌 Project Overview
This project implements a **Transformer-based deep learning model from scratch** to perform **Next Word Prediction** on textual data.

The model learns contextual relationships between words and predicts the most probable next word given an input sequence. This project demonstrates a strong understanding of modern NLP techniques and Transformer architectures without relying on pre-built Transformer libraries.

---

## 🎯 Problem Statement
Given a sequence of words, predict the **next most likely word** using a trained model.

Example:
Input: "to be or not to"
Output: ["the", "be", "me", "my", "him"]


---

## 🧠 Key Concepts
- Natural Language Processing (NLP)
- Tokenization & Vocabulary Encoding
- Sequence Modeling
- Transformer Architecture
- Self-Attention Mechanism
- Deep Learning using PyTorch

---

## ⚙️ Methodology

### 🔹 1. Text Preprocessing
- Converted text to lowercase
- Removed unwanted characters
- Tokenized sentences into words

### 🔹 2. Vocabulary Creation
- Used frequency-based selection (`Counter`)
- Limited vocabulary size for efficiency
- Created:
  - `word2idx` (word → index)
  - `idx2word` (index → word)
- Added `<pad>` token for padding

### 🔹 3. Text Encoding
Converted words into numerical sequences:

"I love AI" → [12, 45, 78]


### 🔹 4. Sequence Padding
- Ensured fixed-length inputs
- Used zero-padding for shorter sequences

---

## 🏗️ Transformer Architecture (From Scratch)

The model was built manually without using external Transformer APIs.

### Components:
- 🧩 Embedding Layer
- 📍 Positional Encoding
- 🔁 Multi-Head Self Attention
- 🧠 Feed Forward Network
- 🔄 Residual Connections
- 📏 Layer Normalization

---

## 🏋️ Training Process
- Loss Function: `CrossEntropyLoss`
- Optimizer: `Adam`
- Used mini-batch training with `DataLoader`
- Validation loss used for:
  - Monitoring performance
  - Saving best model (`best_model.pt`)

---

## 📊 Evaluation Metrics

### 🔹 Perplexity
- Measures prediction confidence
- Lower is better

### 🔹 Accuracy
- Measures correctness of predictions

---

## 📈 Results

| Metric       | Value |
|-------------|------|
| Perplexity  | 2.64 |
| Accuracy    | 94%  |

---

## 🔮 Prediction Example
Input: "to be or not to"
Output: ['the', 'be', 'me', 'my', 'him']


---

## 📁 Project Structure
project/
│
├── model.py # Transformer architecture
├── train.py # Training pipeline
├── predict.py # Next-word prediction
├── utils.py # Preprocessing & tokenization
├── best_model.pt # Trained model weights
├── results.json # Evaluation metrics
├── train_log.txt # Training logs
├── requirements.txt # Dependencies
└── README.md # Documentation


---

## ⚙️ Installation

```bash
pip install -r requirements.txt
▶️ Usage
Train the Model
python train.py
Run Prediction
python predict.py
📦 Requirements
torch
numpy
