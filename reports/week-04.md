# Final Report

## Course
Deep Learning

## Name
Kozhakhan Bizhamal

## Semester
Spring 2026

---

# 1. Project Overview

This project focuses on detecting fake and real news articles using Natural Language Processing (NLP) and Deep Learning techniques. The system classifies news articles into two categories:

- Fake News (0)
- Real News (1)

The project compares classical machine learning approaches with deep learning methods to evaluate their performance on text classification tasks.

---

# 2. Problem Statement

Fake news has become a serious global issue due to the rapid spread of misinformation on social media and online platforms. Manual verification of news articles is difficult because of the large amount of information generated every day.

The goal of this project is to create an automated fake news detection system capable of classifying articles as fake or real using machine learning and deep learning models.

---

# 3. Dataset Description

## Dataset Name
Fake and Real News Dataset

## Dataset Source
https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset

## Dataset Information

| Feature | Description |
|---|---|
| title | News headline |
| text | Full article text |
| label | Target class (0 = Fake, 1 = Real) |

The dataset contains almost 20,000 news articles and is balanced between fake and real classes.

---

# 4. Data Preprocessing

Several preprocessing techniques were applied before training the models.

## Preprocessing Steps

- Lowercasing text
- Removing punctuation
- Removing URLs
- Removing special characters
- Tokenization
- Padding sequences for LSTM

These steps help reduce noise and convert text into a format suitable for machine learning models.

---

# 5. Train-Test Split

The dataset was divided into:

- 80% training data
- 20% testing data

The test set was not used during training to ensure fair evaluation.

---

# 6. Baseline Model

## TF-IDF + Logistic Regression

A baseline model was created using TF-IDF vectorization and Logistic Regression.

## Purpose

The baseline model provides a simple and interpretable benchmark for comparison with deep learning approaches.

## Baseline Results

| Metric | Value |
|---|---|
| Accuracy | 98.64% |

### Classification Results

| Class | Precision | Recall | F1-score |
|---|---|---|---|
| Fake News | 0.99 | 0.98 | 0.99 |
| Real News | 0.98 | 0.99 | 0.99 |

## Observation

The baseline model performed extremely well because the dataset is highly separable using TF-IDF features.

---

# 7. Deep Learning Model

## LSTM Model

The deep learning model used in this project is LSTM (Long Short-Term Memory).

## Why LSTM?

LSTM models are designed for sequential data and can capture contextual relationships between words.

Unlike TF-IDF, LSTM considers word order and sequence information.

---

# 8. LSTM Architecture

The LSTM model consists of:

- Embedding Layer
- LSTM Layer
- Fully Connected Layer
- Sigmoid Activation

---

# 9. Training Configuration

| Parameter | Value |
|---|---|
| Epochs | 3 |
| Batch Size | 64 |
| Learning Rate | 0.001 |
| Optimizer | Adam |
| Loss Function | Binary Cross Entropy |

---

# 10. Training Loss

| Epoch | Loss |
|---|---|
| 1 | 0.2460 |
| 2 | 0.1739 |
| 3 | 0.0821 |

The decreasing loss values indicate successful model learning.

---

# 11. LSTM Evaluation Results

| Metric | Value |
|---|---|
| Accuracy | 98.06% |

### Classification Results

| Class | Precision | Recall | F1-score |
|---|---|---|---|
| Fake News | 0.98 | 0.98 | 0.98 |
| Real News | 0.98 | 0.98 | 0.98 |

---

# 12. Transformer Exploration

## DistilBERT

A pretrained DistilBERT Transformer model was explored to demonstrate understanding of modern NLP architectures.

Due to CPU-only computational limitations and long training time, full fine-tuning was not completed. However, pretrained Transformer inference experiments were performed.

This demonstrates understanding of:

- Transformer-based NLP
- Pretrained language models
- Contextual language understanding
- Modern deep learning workflows

---

# 13. Model Comparison

| Model | Type | Accuracy |
|---|---|---|
| Logistic Regression | TF-IDF Baseline | 98.64% |
| LSTM | Deep Learning | 98.06% |
| DistilBERT | Transformer Exploration | Experimental |

---

# 14. Error Analysis

Although the models achieved high accuracy, several errors still occurred.

## Common Failure Cases

### Short Headlines
Some articles were too short and lacked contextual information.

### Ambiguous Language
Certain fake news articles used professional or neutral language similar to real news.

### Vocabulary Overlap
Fake and real news articles sometimes shared similar keywords.

## Important Observation

Deep learning models do not always outperform simpler machine learning models. In this project, Logistic Regression slightly outperformed LSTM because the dataset was highly separable.

---


# 15. Challenges and Limitations

## Challenges

- Large text preprocessing requirements
- Long Transformer training time
- Hardware limitations
- Hyperparameter tuning complexity

## Limitations

- Dataset may be cleaner than real-world news
- Models may not generalize perfectly to unseen online content
- DistilBERT was not fully fine-tuned

---

# 16. Conclusion

This project successfully implemented a complete fake news detection pipeline using both machine learning and deep learning techniques.

The project included:

- Data preprocessing
- Baseline machine learning model
- LSTM deep learning model
- Transformer exploration
- Model comparison
- Error analysis

The results demonstrate that both traditional and deep learning approaches can perform effectively on NLP classification tasks.

An important conclusion from this project is that simpler models can sometimes outperform more complex deep learning architectures depending on dataset characteristics.

---

# 17. Future Improvements

Possible future improvements include:

- Full BERT fine-tuning using GPU
- Larger and noisier datasets
- Explainable AI techniques
- Real-time deployment
- Multi-language fake news detection

---

# 18. References

1. Kaggle Fake and Real News Dataset  
https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset

2. PyTorch Documentation  
https://pytorch.org/

3. Hugging Face Transformers  
https://huggingface.co/docs/transformers/index

4. Scikit-learn Documentation  
https://scikit-learn.org/

