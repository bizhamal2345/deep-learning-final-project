Project: Fake News Detection using Deep Learning
1. Work Completed This Week

This week focused on data preprocessing and building a baseline machine learning model for fake news detection.

Completed tasks:

Loaded the Fake and Real News dataset
Merged datasets and shuffled the data for randomness
Performed text preprocessing:
Converted text to lowercase
Removed punctuation, URLs, and special characters
Split dataset into training and testing sets (80/20 split)
Applied TF-IDF vectorization to convert text into numerical features
Built a baseline Logistic Regression model
Evaluated model performance using multiple metrics

2. Model Used (Baseline)
Algorithm: Logistic Regression
Feature extraction: TF-IDF (max 5000 features)
Task: Binary classification (Fake vs Real news)


3. Evaluation Results
Accuracy:
0.9864 (98.64%)
Classification Report:
Class	    Precision	Recall	F1-score	Support
Fake (0)	0.99	    0.98	  0.99	    4701
Real (1)	0.98	    0.99	  0.99	    4279
Overall:
Accuracy: 98.6%
Macro Avg F1-score: 0.99
Weighted Avg F1-score: 0.99


4. Prediction Distribution
Fake news detected: 4671
Real news detected: 4309


5. Observations
The baseline Logistic Regression model performs very well on this dataset.
TF-IDF features are effective for capturing word-level patterns.
The dataset appears to have strong separability between fake and real news.
However, the model does not understand context or sequence meaning.


6. Limitations
The model relies only on word frequency (no semantic understanding)
Cannot capture long-term dependencies in text
May fail on more complex or manipulated fake news
High performance may indicate dataset bias or simplicity


7. Challenges
Text preprocessing significantly affects performance
Some fake and real articles are very similar in structure
Model may overfit to dataset-specific patterns


8. Next Week Plan (Week 3)
Implement deep learning model using LSTM (PyTorch)
Convert text into sequences using tokenization and padding
Train neural network and compare with baseline
Evaluate using same metrics (accuracy, F1-score)
Begin model comparison analysis
