#  Fake News Detection using Deep Learning

---

##  Project Overview

This project focuses on detecting fake news articles using **Natural Language Processing (NLP)** and **Deep Learning techniques**.  

The model classifies news as either:
- **Fake (0)**
- **Real (1)**

based on the textual content of the article.

Fake news has become a serious global issue, and automated detection systems can help reduce the spread of misinformation on online platforms.

---

##  Problem Statement

The goal of this project is to build a machine learning system that can automatically classify news articles into two categories:

- Fake News
- Real News

The system uses both:
- Traditional Machine Learning (baseline model)
- Deep Learning approaches

to compare performance and effectiveness.

---

##  Dataset

### Dataset Name
Fake and Real News Dataset

### Source
Kaggle:  
https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset

### Dataset Details
- almost 20,000 news articles
- Binary classification task

### Features
- `title` → News headline  
- `text` → Full article content  

### Labels
- `0` → Fake News  
- `1` → Real News  

---

##  Project Pipeline

### 1. Data Preprocessing
- Lowercasing text
- Removing punctuation and special characters
- Tokenization
- Padding sequences (for deep learning models)

---

### 2. Baseline Model (Machine Learning)
- TF-IDF Vectorization
- Logistic Regression Classifier

**Purpose:**  
To create a simple and interpretable benchmark model.

---

### 3. Deep Learning Model
- LSTM (Long Short-Term Memory network) using PyTorch

**Optional upgrade:**
- Transformer-based model (e.g., DistilBERT)

**Purpose:**  
To capture sequential and contextual meaning in text data.
