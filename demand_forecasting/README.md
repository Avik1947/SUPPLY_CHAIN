# 📦 Demand Forecasting – Ecuador Sales

A forecasting pipeline built on the volatile tremors of Ecuador’s real-world retail data. Earthquakes, oil prices, erratic holidays — all thrown into a time series stew to predict daily item-level sales.

This project was developed for the **Kaggle "Store Sales - Time Series Forecasting"** competition
---

## 🔍 Problem Statement

Forecast the unit sales of 50+ product families across 50+ stores using multi-year time series data, incorporating:

- **Holidays & Events**
- **Oil Prices**
- **Promotions**
- **Earthquake Impact (2016)**

---

## 🧠 Notebook Overview

### 🛠️ Data Engineering

- 🔗 Merges: `train`, `oil`, `holidays`, `stores`, `transactions`
- 🧹 Null Handling: NaNs filled 
- 🧠 Feature Extraction:
  - Temporal: day, week, month, year, weekday
  - Lag Features: 7, 14, 30 days
  - Rolling Means: 30-day trailing window
- 🎚️ Label + One-Hot Encoding
- 📉 Log Scaling: Numerical columns were log-scaled to kill skewness

---

## 📊 Exploratory Data Analysis (EDA)

### 🛢️ Oil Prices
- Most values **hover around \$70**
- Some outliers present: **spikes >90 and dips <55**
- Stable trend

### 🏙️ Cities
- **Quito** is the main hub
- **Guayaquil** follows after

### 🗺️ States
- Most records come from **Pichincha** and **Guayas**
- Quito is the capital of Pichincha → geographic granularity matters

### 💳 Transactions
- Average: **1700 transactions**
- Standard Deviation: ~**900** → strong variability across time and stores

### 🛍️ Type Variable
- Categorical variable `type` exists, but meaning is unclear
- Hypothesis: it might influence sales behavior — **worth further analysis**
- feature importance shows **not to worry for 'type'**

---

## ⚙️ Modeling

- Multiple regression models tried:
  - `LinearRegression`, `GradientBoosting`
  - `XGBoost`, `histgbm`, `CatBoost`
- Feature selection via model-based importance
- Redundant variables pruned
- **Data truncated post-2016** due to instability (Earthquake Year)

### 📈 Final Model Observations:
1. **Feature importance plots** guided variable selection
2. **Redundant variables were cleaned**
3. **Post-2016 data retained** due to 2016’s seismic instability
4. **Model performance improved significantly** after truncation and feature cleanup

---

## 🧪 Evaluation

- **Metric**: Root Mean Squared Logarithmic Error (RMSLE)
- **Final Public Score**: `1.90`

---

## 🧰 Libraries Used

- `Pandas`, `NumPy`, `Seaborn`, `Matplotlib`
- `Scikit-learn`
- `XGBoost`, `CatBoost`

---

## 🧠 TL;DR (if you're skimming)

- Dfs joins. Temporal features. Data cleanup.
- Earthquake? We dodged it.
- Skewed data? Stabilized.
- Sales forecast? Delivered.


