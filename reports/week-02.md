#  Project: Fake News Detection using Deep Learning  
##  Week 2 Report

---

##  Work Completed This Week

This week focused on **data preprocessing** and building a **baseline machine learning model** for fake news detection.

---

###  Completed Tasks

- Loaded the Fake and Real News dataset  
- Merged datasets and shuffled data for randomness  
- Performed text preprocessing:
  - Converted text to lowercase  
  - Removed punctuation, URLs, and special characters  
- Split dataset into training and testing sets (80/20 split)  
- Applied TF-IDF vectorization to convert text into numerical features  
- Built a baseline Logistic Regression model  
- Evaluated model performance using multiple metrics  

---

##  Model Used (Baseline)

### Algorithm
- Logistic Regression

### Feature Extraction
- TF-IDF (max 5000 features)

### Task
- Binary classification (Fake vs Real news)

---

##  Evaluation Results

### Accuracy
- **98.64%**

---

### Classification Report

| Class | Precision | Recall | F1-score | Support |
|------|-----------|--------|----------|---------|
| Fake (0) | 0.99 | 0.98 | 0.99 | 4701 |
| Real (1) | 0.98 | 0.99 | 0.99 | 4279 |

---

### Overall Metrics
- Accuracy: **98.6%**
- Macro Avg F1-score: **0.99**
- Weighted Avg F1-score: **0.99**

---

##  Prediction Distribution

- Fake news detected: **4671**
- Real news detected: **4309**

---

##  Observations

- The Logistic Regression baseline performs very well on this dataset  
- TF-IDF features effectively capture word-level patterns  
- The dataset shows strong separability between fake and real news  
- However, the model does not understand context or sequence meaning  

---

##  Limitations

- Relies only on word frequency (no semantic understanding)  
- Cannot capture long-term dependencies in text  
- May fail on complex or heavily manipulated fake news  
- High accuracy may indicate dataset bias or simplicity  

---

##  Challenges

- Text preprocessing significantly affects performance  
- Some fake and real articles are very similar in structure  
- Model may overfit dataset-specific patterns  

---

##  Next Week Plan (Week 3)

- Implement deep learning model using LSTM (PyTorch)  
- Convert text into sequences using tokenization and padding  
- Train neural network and compare with baseline  
- Evaluate using same metrics (accuracy, F1-score)  
- Begin model comparison analysis  
