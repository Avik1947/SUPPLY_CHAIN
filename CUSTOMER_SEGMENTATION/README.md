# 🧬 Customer Segmentation, CLV & Product Affinity in Brazilian E-Commerce

### 📦 SQL-fueled journey through loyalty, lifetime value, and buying behavior

This project slices deep into the Brazilian e-commerce dataset with one agenda: **understand your customer before they ghost you**.  
We blend **SQL**, **RFM analysis**, **CLV estimation**, and **network theory** to unmask segments, predict sales, and map co-purchase patterns.

---

## 🎯 What We Did (And Why)

### 🧱 Goals:
- Segment customers based on **Recency**, **Frequency**, and **Monetary Value**
- Estimate **Customer Lifetime Value** (CLV)
- Forecast **category-level sales** using regression
- Visualize **co-purchase networks** for upselling opportunities
- Dissect **shipping time patterns** and holiday/postal impacts

---

## 🔍 Key Insights

### 💳 Purchase Behavior:
- **96.9%** of orders come from **one-time buyers**  
- But **3.1%** repeat customers punch above their weight in value

### 💰 Product Pricing:
- Most orders: under **R$200**
- Shipping: typically **R$7–R$20**, but some go sky-high

---

## 🧠 Customer Segmentation: RFM in Action

We scored each customer on:

- **Recency** – Days since last purchase
- **Frequency** – Number of orders
- **Monetary** – Total spend

### 🏷️ RFM Buckets (Top Performers):

| Segment               | Avg Days Since Purchase | Avg Spend (R$) | Count |
|-----------------------|--------------------------|----------------|-------|
| Champions             | 2537                     | 250.86         | 4607  |
| Loyal Customers       | 2668                     | 237.88         | 9315  |
| Can’t Lose Them       | 2884                     | **350.88**     | 1723  |
| About to Sleep        | 2710                     | 57.68          | 7584  |
| Lost                  | 2887                     | 57.39          | 15331 |

**Strategic play:**  
- Nurture **Champions**, entice **Potential Loyalists**, re-engage the **Can’t Lose Them**.
- Don’t spend marketing dollars on the **Lost**—their ship has sailed.

---

## 📈 Sales Forecasting

Using linear regression, we predicted category trends for the holiday period:

| Category         | Trend Summary |
|------------------|---------------|
| health_beauty    | High sales, declining toward Christmas |
| toys             | Sharp early peak, drops mid-month |
| auto             | Stable early, then declining |
| electronics      | Mirrors auto trend |
| fashion_shoes    | **Resilient**, slight increase in late December |

> *Fashion shoes defy Santa. Everything else rides the holiday rollercoaster.*

---

## 🚚 Delivery Performance Analysis

### From Order to Customer:

- **Approval to dispatch**: ~3 days across cities  
- **Dispatch to delivery**:
  - **São Paulo, Guarulhos, São Bernardo**: ~5 days  
  - **Rio, Porto Alegre, Salvador**: 2× longer  

> **Predicted delivery dates are padded pessimistically.**  
Actuals are quicker—except in two black holes:
- **December 2017**: Holiday chaos
- **Feb–Mar 2018**: Postal strikes

---

## 🧠 CLV (Customer Lifetime Value)

We calculated CLV using:

- Average order value × purchase frequency × expected lifespan  
- Adjusted with discounting to reflect net present value

> Helps prioritize **who's worth chasing—and who's burning your ad budget.**

---

## 🔗 Product Affinity Graph (Co-Purchase Network)

> Picture every product as a node. Connections = bought together. Bigger node = more orders.

### Notable clusters:

- 🌱 **Garden tools**: tight-knit, often bought in sets
- 🛁 **Bed, Bath, Table** ↔ **Home Comfort**: cross-category linkage
- 🚗 **Auto accessories** & 🖱 **Computer gear**: strong intra-category ties

> **Insights?** Bundle garden kits. Cross-promote comfort + décor. Upsell mousepads with USB hubs.

---

## 🧰 Tech Stack

- **Language**: SQL (SQLite)
- **Visualization**: matplotlib, seaborn, networkx
---


## 🚀 What’s Next?

- 🧠 Cluster-based segmentation using K-Means on RFM + behavior features
- 🔁 Build a recommendation system using co-purchase network

---
