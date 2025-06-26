# 🇧🇷 Brazilian E-Commerce: EDA + NLP Sentiment Analysis

### 📦 Decoding Consumer Pulse in Brazil’s Online Marketplace

This project dives headfirst into a real-world Brazilian e-commerce dataset. We followed the buyer trail, cracked customer behavior patterns, and parsed thousands of product reviews to decode sentiment.
---

## 🔍 Problem We Tackled

1. **Understand consumer behavior** — Who buys what, when, and from where?
2. **Evaluate delivery performance** — Are promises being kept?
3. **Mine product reviews** — Are customers truly satisfied, or just quiet?
4. **Build sentiment classifiers** — Let the machines feel.

---

## 📊 Exploratory Data Analysis: What Brazil Taught Us

| Insight | Findings |
|--------|----------|
| ✅ Deliveries | 97% orders delivered on time. Only 3% lingered in other status. |
| 📈 Order Volume | Monotonically rising. Brazil’s buying mood = bullish. |
| 🕒 Purchase Timing | Mondays, between 12 PM – 5 PM, are the peak buying hours. |
| 🌆 Geography | São Paulo and Rio dominate. SP is the kingpin of e-commerce volume. |
| 💳 Payment Trends | Credit card is the weapon of choice for most Brazilians. |

---

## 🧠 Sentiment Analysis: The Review Oracle

### 🧼 Text Preprocessing:
- Lowercasing, removing line breaks, dates, URLs, numbers
- Stopword filtering (except the sacred **"not"**—because **"not happy" ≠ "happy"**)
- TF-IDF Vectorization

### 🤖 Models Tested:

| Model | Accuracy | Precision | Recall | F1 Score | ROC AUC |
|-------|----------|-----------|--------|----------|---------|
| Logistic Regression | **0.8896** | **0.9333** | 0.8933 | **0.9129** | **0.9431** |
| Random Forest       | 0.8895 | 0.9137 | 0.9158 | 0.9147 | 0.9372 |
| LightGBM            | 0.8886 | 0.9298 | 0.8956 | 0.9124 | 0.9414 |
| Gradient Boosting   | 0.8603 | 0.8599 | **0.9369** | 0.8967 | 0.9240 |
| KNN                 | 0.8377 | 0.8369 | 0.9306 | 0.8813 | 0.8596 |
| XGBoost             | 0.8278 | 0.8000 | **0.9787** | 0.8804 | 0.9385 |

> Logistic Regression took the crown—simple, elegant, powerful. But Gradient Boosting had the best ears for complaints (recall: 93.7%).

---

## 🧰 Tech Stack

- **Language:** Python 🐍
- **Libraries:** pandas, matplotlib, seaborn, scikit-learn, xgboost, lightgbm
- **NLP Tools:** TF-IDF, regex cleaning, sentiment modeling

---

## 🧠 What's Next?

- 🧬 Add topic modeling (LDA) to cluster review themes
- 🧭 Predict delivery delays based on customer location and product type
- 🎯 Fine-tune ensemble sentiment models with hyperparameter optimization

---
