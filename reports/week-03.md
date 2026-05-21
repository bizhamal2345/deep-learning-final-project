#  Project: Fake News Detection using Deep Learning  
##  Week 3 Report

---

##  Work Completed This Week

This week focused on developing a **deep learning model (LSTM)** for fake news classification and comparing its performance with the baseline Logistic Regression model.

---

###  Completed Tasks

- Converted text data into tokenized sequences  
- Applied padding to ensure uniform input length  
- Built and trained an LSTM model using PyTorch  
- Trained the model for 3 epochs  
- Evaluated model performance using:
  - Accuracy  
  - Precision  
  - Recall  
  - F1-score  
- Compared results with the baseline model  

---

##  Deep Learning Model

### Model Type
- LSTM (Long Short-Term Memory network)

### Framework
- PyTorch

### Input
- Tokenized and padded sequences

### Output
- Binary classification (Fake / Real news)

---

##  Training Details

- Epochs: 3  
- Loss function: Binary Cross Entropy Loss  
- Optimizer: Adam  
- Batch size: 64  
- Learning rate: 0.001  

---

###  Training Loss Progress

- Epoch 1: 0.2460  
- Epoch 2: 0.1739  
- Epoch 3: 0.0821  

**Observation:**  
The loss consistently decreased, indicating successful learning and model convergence.

---

##  Evaluation Results

### Accuracy
- **98.06%**

---

### Classification Report

| Class | Precision | Recall | F1-score | Support |
|------|-----------|--------|----------|---------|
| Fake (0) | 0.98 | 0.98 | 0.98 | 4701 |
| Real (1) | 0.98 | 0.98 | 0.98 | 4279 |

---

### Overall Metrics
- Accuracy: **98.06%**
- Macro Avg F1-score: **0.98**
- Weighted Avg F1-score: **0.98**

---

##  Model Comparison

| Model Type | Accuracy | Notes |
|------------|----------|-------|
| Logistic Regression (TF-IDF baseline) | 98.64% | Very strong classical baseline |
| LSTM (Deep Learning) | 98.06% | Captures sequential meaning |

---

##  Observations

- LSTM successfully learned contextual patterns in text data  
- However, Logistic Regression performed slightly better on this dataset  
- This suggests the dataset is highly linearly separable using TF-IDF features  
- Deep learning does not always outperform classical models on simpler NLP datasets  

---

##  Insights

- TF-IDF + Logistic Regression is a very strong baseline for text classification  
- LSTM provides better theoretical understanding of sequence data but requires tuning  
- Model performance depends heavily on dataset complexity, not just model type  

---

##  Challenges

- Training LSTM is more computationally expensive than baseline models  
- Performance is sensitive to sequence length and padding  
- Limited epochs may restrict full LSTM potential  

---

##  Next Week Plan (Week 4)

- Improve model performance (hyperparameter tuning)  
- Implement Transformer-based model (DistilBERT) for advanced comparison  
- Build Streamlit application for real-time fake news prediction  
- Perform error analysis (misclassified examples)  
- Finalize report and prepare presentation  
