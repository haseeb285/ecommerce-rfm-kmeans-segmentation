# ecommerce-rfm-kmeans-segmentation
Customer segmentation for retail e-commerce using RFM analysis and K-Means clustering. Includes end-to-end pipeline with data cleaning, EDA, clustering, and actionable business recommendations.
# 🛒 Customer Segmentation for Retail E-Commerce (RFM + K-Means)

<p align="left">
  <img alt="Python" src="https://img.shields.io/badge/Python-3.x-blue">
  <img alt="NumPy" src="https://img.shields.io/badge/NumPy-Numerics-informational">
  <img alt="Pandas" src="https://img.shields.io/badge/Pandas-Data%20Wrangling-informational">
  <img alt="Matplotlib" src="https://img.shields.io/badge/Matplotlib-Visualization-informational">
  <img alt="Seaborn" src="https://img.shields.io/badge/Seaborn-Visualization-informational">
  <img alt="SciPy" src="https://img.shields.io/badge/SciPy-Stats-informational">
  <img alt="scikit-learn" src="https://img.shields.io/badge/scikit--learn-ML%20%26%20Clustering-orange">
  <img alt="Colab" src="https://img.shields.io/badge/Google%20Colab-Notebook-yellow">
</p>

## 🛠 Tech Used
- **Language:** Python  
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, SciPy, scikit-learn  
- **Methods:** Data Cleaning, EDA, **RFM Analysis**, **K-Means Clustering**, **Silhouette Analysis**, Scaling/Outlier handling  
- **Environment:** Google Colab / Jupyter Notebook

---

## 📌 Overview
**End-to-end customer segmentation** pipeline for a retail e-commerce startup.  
The workflow covers **Data Cleaning → Exploratory Data Analysis → RFM feature engineering → K-Means clustering** → business **insights & recommendations** per segment.

> Use segmentation to improve **targeted marketing**, reduce wasted budget, and increase repeat purchases and LTV.

---

## 🎯 Objective
Help **Olist** improve marketing conversion rates by targeting the **right customers with the right incentives**, instead of broad, inefficient campaigns.

---

## 🧪 Data & Business Context
Olist is a fast-growing e-commerce brand that saw a surge during COVID-19. Despite growth, a lack of targeted marketing means only a fraction of users return.  
Segmenting customers enables **personalized campaigns** and **smarter spend allocation**.

---

## 🧮 RFM Framework
We compute three key behavioral features per customer:

- **Recency (R):** Days since last purchase  
- **Frequency (F):** Number of transactions  
- **Monetary (M):** Total spend

Typical steps:
1. Aggregate transactions by customer ID  
2. Compute `Recency`, `Frequency`, `Monetary`  
3. Scale features (e.g., `StandardScaler` / `RobustScaler`)  
4. Determine K via **Elbow** and **Silhouette**  
5. Fit **K-Means**, evaluate with silhouette score, and profile clusters

---

## 🔍 EDA Highlights (examples)
- Identify distribution of order values and order counts per customer  
- Check recency spread and long-tail behavior  
- Correlate R, F, M to understand purchase patterns  
- Remove/Cap outliers where necessary to stabilize clustering

---

## 🤖 Clustering
- **Algorithm:** K-Means  
- **Model selection:** Elbow plot + **Silhouette Analysis**  
- **Inputs:** Scaled R, F, M (optionally log-transformed M to reduce skew)  
- **Outputs:** Cluster labels + descriptive profiles

---

## 👥 Segments, Insights & Recommendations
**1) The Loyal One 🧡🧡** — *high spend, buy recently (low recency)*  
- **Strategy:** Keep them engaged—**loyalty points**, early access, VIP support  
- **Note:** Avoid over-discounting; protect margins while rewarding loyalty

**2) The Probably Churned ❗❗** — *moderate spend, long since last purchase (high recency)*  
- **Strategy:** Win-back with **limited-time, high-benefit vouchers** + email/push nudges  
- **Goal:** Reactivate quickly; measure uplift vs. control

**3) The Casual One 😀** — *low spend, moderate recency*  
- **Strategy:** **Cashback** or **threshold-based** coupons (e.g., “Spend ≥ 100 to get X”) to lift AOV and encourage repeat purchase

