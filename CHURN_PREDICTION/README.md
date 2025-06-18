# 🔁 Churn Prediction for Neo-Banks

## 💼 Problem
In neo-banking, **customer churn is silent but deadly** — high acquisition costs make every retained user critical. The challenge? Early signals of churn are subtle, and typical models are either too reactive or too general.

## 🎯 Objective
Build a **high-precision, low-loss** ML pipeline that predicts user churn well before it happens — to enable **preventive retention strategies**.

## 💡 Key Result

> 🧠 **Log-Loss Achieved**: **0.009**  
> 🎯 **Model**: XGBoost (Tuned)  

---

## ⚙️ Solution Workflow

- ✅ Cleaned behavioral + transactional logs  
- 📐 Feature engineered time-series and lifecycle traits  
- 🎛️ Trained & tuned classifiers using **log-loss**  
- 🔁 Validated robustness using cross-validation and hold-out sets  

---

## 🧠 Why These Decisions?

### 1. Signal Extraction Over Noise
Behavior patterns are nuanced. We designed features that capture:
- **Session frequency decay**
- **Time since last interaction**
- **Payment vol**
- **Usage entropy across services**
---

### 2. Log-Loss as Optimization Metric
Churn is probabilistic. Predicting "yes" or "no" isn't enough — we optimized for **log-loss** to measure **confidence calibration**.

→ This enables ranked churn lists and smarter retention budgets.

---

## 📊 Final Metrics

- **Log-Loss**: `0.009`

→ Model outputs can be directly used for **priority-based retention** workflows.

---

## 📈 Business Impact

This model allows a neo-bank to:
- Proactively intervene **weeks before churn**  
- Segment by churn risk level  
- Prioritize high-LTV users for manual outreach  
- Allocate retention budgets efficiently

---

## 🚀 Next Steps

- Integrate into **real-time scoring pipeline**  
- Build **dashboards for marketing teams**  
- Train **uplift models** for actionability (who to save vs. let go)

---

## 🧠 TL;DR

A log-loss-optimized churn prediction engine tailored for neo-banks.
