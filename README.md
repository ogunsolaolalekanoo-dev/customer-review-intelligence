# customer-review-intelligence
End-to-end NLP pipeline for sentiment analysis, threshold optimization, and customer segmentation using Amazon reviews to drive business decisions.
# 📊 From Reviews to Revenue: Customer Sentiment Analysis & Topic Discovery

## 🚀 Project Overview

Customer reviews contain valuable insights about product performance, customer satisfaction, and business risks. However, most of this data is unstructured and difficult to analyze at scale.

This project builds an end-to-end **text mining pipeline** to:

- Classify customer sentiment (negative, neutral, positive)
- Optimize decision-making using threshold tuning
- Discover hidden product segments using clustering

The goal is to transform raw customer feedback into **actionable business intelligence**.

---

## 💼 Business Problem

E-commerce companies receive millions of customer reviews daily, but:

- Reviews are unstructured and difficult to analyze
- Customer dissatisfaction is often detected too late
- Product issues are hidden within large volumes of text

👉 Without automation, businesses cannot effectively respond to customer needs at scale.

---

## 🎯 Solution Approach

This project applies machine learning and NLP techniques to:

### 1. Sentiment Classification
- Predict customer sentiment using:
  - Naive Bayes
  - Logistic Regression
  - Support Vector Machine (SVM)

### 2. Threshold Tuning
- Customize decision thresholds to align with business goals:
  - Detect dissatisfied customers early
  - Optimize marketing targeting

### 3. Topic Discovery (Clustering)
- Use K-Means clustering to identify product-related themes:
  - Coffee
  - Tea
  - Pet products
  - Snacks and general items

---

## 📂 Dataset

- Source: Amazon Reviews Dataset  
- Type: Unstructured text data  
- Domain: Food and consumer products  

### Features Used:
- Review Summary
- Review Text
- Rating Score (converted to sentiment)

### Sentiment Mapping:
- Negative → Score 1–2  
- Neutral → Score 3  
- Positive → Score 4–5  

---

## 🧹 Data Processing Strategy

Two preprocessing pipelines were used:

### 🔹 Baseline Pipeline (For Classification)
- Minimal cleaning
- Preserves sentiment signals
- Optimized for predictive performance

### 🔹 Cleaned Pipeline (For Clustering)
- Stopword removal
- Lemmatization
- Noise reduction
- Optimized for interpretability

---

## ⚙️ Feature Engineering

- Bag-of-Words (Naive Bayes)
- TF-IDF (Logistic Regression, SVM)
- N-grams (bigrams) to capture context
- Frequency filtering using `min_df` and `max_df`

---

## 🤖 Model Performance

| Model | Accuracy | ROC-AUC | Log Loss |
|------|--------|--------|---------|
| Naive Bayes | ~0.71 | ~0.86 | ~1.29 |
| Logistic Regression | ~0.81 | ~0.93 | ~0.50 |
| SVM | ~0.81 | N/A | N/A |

### Key Insight:
- **SVM achieved the highest accuracy**
- **Logistic Regression provided the best balance of performance and probability quality**

---

## 🎯 Threshold Optimization

### 🔴 Negative Customer Detection (Critical)

- Recommended Threshold: **0.35**
- Priority: **High Recall**

👉 Ensures most dissatisfied customers are detected early

---

### 🟢 Positive Customer Detection

- Recommended Threshold: **0.45**
- Balanced Precision and Recall

👉 Supports targeted marketing and customer engagement

---

## 📊 Key Metrics Explained

- **Precision** → Accuracy of predictions  
- **Recall** → Ability to capture actual cases  
- **F1 Score** → Balance between precision and recall  
- **ROC-AUC** → Model's ability to separate classes  
- **Log Loss** → Confidence of probability predictions  

### Business Focus:
👉 Minimizing **False Negatives** (missed unhappy customers)

---

## 🧠 Clustering Insights

K-Means clustering revealed key product segments:

- ☕ Coffee Products  
- 🍵 Tea Products  
- 🐶 Pet Products  
- 🍫 Snacks and Sweets  
- 📦 General Products  

### Business Value:
- Customer segmentation  
- Product trend analysis  
- Targeted recommendations  

---

## 💡 Business Recommendations

- Deploy Logistic Regression for real-world applications
- Use threshold tuning to prioritize risk detection
- Monitor negative reviews proactively
- Use clustering for product segmentation
- Improve high-complaint product categories
- Build dashboards for sentiment tracking

---

## 📈 Key Visualizations

- Confusion Matrix
- Threshold Tuning Curve
- Cluster Distribution



---

## 🔮 Future Improvements

- Deploy as API (Flask / FastAPI)
- Real-time sentiment dashboard
- Integration with customer support systems
- Advanced NLP models (BERT, transformers)

---

## 🛠️ Tech Stack

- Python  
- Pandas, NumPy  
- Scikit-learn  
- Matplotlib  

---

## 📌 Conclusion

This project demonstrates how unstructured customer reviews can be transformed into actionable insights through machine learning.

👉 The real value lies not in prediction alone, but in enabling **data-driven business decisions**.

---

## 👤 Author

**Olalekan Ogunsola**  
Data Engineer | Analytics Engineer | Machine Learning  

---
