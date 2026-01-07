# Sentiment Analysis on Amazon Product Reviews

## Overview
This project implements an end-to-end **Sentiment Analysis system** for Amazon product reviews using **Natural Language Processing (NLP)** and **Machine Learning** techniques.  
It is designed to demonstrate real-world data science skills including text preprocessing, feature engineering, model training, evaluation, and prediction.

---

## Business Problem
Customer reviews contain valuable insights about product quality and user experience.  
Manually analyzing thousands of reviews is inefficient and error-prone.

**Goal:**  
Automatically classify Amazon product reviews into:
- Positive
- Neutral
- Negative

This enables:
- Faster feedback analysis
- Improved product decisions
- Better customer satisfaction tracking

---

## Dataset Description
- Source: Amazon Product Reviews (CSV format)
- Key Columns:
  - `review_text` – Customer review content
  - `rating` – Product rating (1–5)

### Sentiment Mapping Logic
| Rating | Sentiment |
|------|---------|
| 4–5 | Positive |
| 3 | Neutral |
| 1–2 | Negative |

---

## Project Architecture
```
amazon-sentiment-analysis/
│
├── data/
│   └── amazon_reviews.csv
│
├── src/
│   ├── preprocess.py
│   ├── train_model.py
│   └── predict.py
│
├── models/
│   ├── sentiment_model.pkl
│   └── vectorizer.pkl
│
├── requirements.txt
└── README.md
```

---

## Technical Stack
- **Programming Language:** Python
- **Libraries:**
  - Pandas, NumPy
  - NLTK
  - Scikit-learn
- **Modeling:**
  - TF-IDF Vectorization
  - Logistic Regression
- **Model Persistence:** Pickle

---

## NLP Pipeline
1. Text Cleaning (lowercasing, removing special characters)
2. Stopword Removal
3. Lemmatization
4. Feature Extraction using TF-IDF
5. Sentiment Classification using Logistic Regression

---

## Model Training
- Train/Test Split: 80/20
- Vectorizer: TF-IDF (max 5000 features)
- Classifier: Logistic Regression

The trained model and vectorizer are saved for reuse.

---

## Model Evaluation
The model is evaluated using:
- Accuracy
- Precision
- Recall
- F1-Score

Expected accuracy is approximately **80–85%**, depending on dataset quality.

---

## How to Run the Project

### Step 1: Install Dependencies
```
pip install -r requirements.txt
```

### Step 2: Train the Model
```
python src/train_model.py
```

### Step 3: Predict Sentiment
```
python src/predict.py
```

---

## Example Prediction
**Input Review:**  
> The product quality is excellent and delivery was fast.

**Predicted Output:**  
> Positive

---

## Use Cases
- Customer feedback analysis
- Product performance monitoring
- Market research
- Review moderation systems

---

## Future Enhancements
- Transformer-based models (BERT)
- Aspect-based sentiment analysis
- Streamlit or Flask web application
- Real-time review ingestion
- Model deployment on cloud platforms

---

## Author
**Sonali Raturi**  
Data Scientist | QA Automation Engineer | NLP Enthusiast  


