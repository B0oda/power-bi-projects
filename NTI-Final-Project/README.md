# 🛒 E-Commerce Marketplace Analysis

A full end-to-end data analytics project covering customer behavior, product performance, and business KPIs for an online marketplace — built as part of the NTI Data Analytics Training Program.

---

## 📌 Project Overview

This project analyzes a retail sales dataset to surface actionable insights for business decision-makers. It covers the complete analytics workflow: data preparation → KPI calculation → visualization → business recommendations.

---

## 📁 Dataset

The dataset contains customer transactions with the following key fields:

| Column | Description |
|---|---|
| Order ID | Unique order identifier |
| Order Date / Ship Date | Transaction and shipping timestamps |
| Ship Mode | Shipping method (Standard, Second Class, etc.) |
| Customer ID / Name | Customer identifiers |
| Segment | Customer segment (Consumer, Corporate, etc.) |
| Region / City | Geographic data |
| Product ID / Category / Sub-Category | Product hierarchy |
| Sales / Quantity / Discount / Profit | Financial metrics |

---

## 🗂️ Project Structure

```
ecommerce-analysis/
│
├── data/
│   └── sales_dataset.csv           # Raw dataset
│
├── notebooks/
│   ├── 01_data_preparation.ipynb   # Cleaning, validation, feature engineering
│   ├── 02_business_kpis.ipynb      # KPI calculations
│   ├── 03_rfm_segmentation.ipynb   # RFM & customer segmentation
│   └── 04_churn_prediction.ipynb   # Bonus: ML churn model
│
├── sql/
│   └── queries.sql                 # SQL queries for data prep & KPIs
│
├── dashboards/
│   └── marketplace_dashboard.pbix  # Power BI dashboard
│
├── reports/
│   └── executive_summary.pdf       # Final business report
│
└── README.md
```

---

## ✅ Part A — Data Preparation

- Loaded dataset into Python (pandas) and SQL
- Validated data quality: missing values, duplicates, inconsistent entries
- Engineered the following customer flags:

| Feature | Definition |
|---|---|
| Active Customer | Made a purchase in the last 90 days |
| Repeat Customer | Placed more than one order |
| New Customer | First purchase occurred in the current month |
| Churned Customer | Purchased in a prior month but not the current month |

---

## 📊 Part B — Business KPIs

All metrics are calculated at a **monthly** granularity unless stated otherwise.

| KPI | Formula |
|---|---|
| Active Customers | Distinct customers with orders in the period |
| New Customers | Customers whose first order is in the current month |
| Churn Rate | Lost customers ÷ Previous month's customers |
| Retention Rate | Retained customers ÷ Previous month's customers |
| Average Order Value (AOV) | Total Sales ÷ Number of Orders |
| Customer Lifetime Value (LTV) | Total Revenue ÷ Unique Customers |

**Additional analyses:**
- Top products, categories, and sub-categories by sales and profit
- RFM segmentation (Recency, Frequency, Monetary)
- Customer grouping by frequency and monetary value

---

## 📈 Part C — Visualizations & Dashboard

Built in **Power BI** (and Python for EDA), the dashboard covers:

- 📅 Monthly sales trends
- 👥 Customer cohort analysis & retention curves
- 🏆 Top products, categories, and sub-categories
- 🚚 Shipping mode adoption breakdown
- 🗺️ Regional and city-level performance
- 💰 Profitability trends and discount impact

---

## 💡 Part D — Business Recommendations

Key findings and recommendations covering:

- **Churn reduction** — identifying at-risk customers and re-engagement strategies
- **Category promotion** — which sub-categories drive the most profit
- **Discount strategy** — how over-discounting erodes margins
- **Regional focus** — underperforming regions and growth opportunities
- **Shipping optimization** — delivery speed vs. customer satisfaction trade-offs

---

## ⭐ Bonus — Churn Prediction Model

A machine learning classification model built to predict churned customers:

- **Features:** RFM scores, order frequency, days since last purchase, segment
- **Model:** Logistic Regression / Random Forest (see notebook for comparison)
- **Evaluation:** Precision, Recall, F1-Score, ROC-AUC

---

## 🛠️ Tools & Technologies

| Tool | Usage |
|---|---|
| Python (pandas, matplotlib, seaborn) | Data cleaning, KPI calculation, EDA |
| SQL | Data preparation and aggregations |
| Power BI | Interactive dashboard |
| scikit-learn | Churn prediction model |

---

## 🚀 How to Run

1. Clone the repository
2. Install dependencies:
   ```bash
   pip install pandas matplotlib seaborn scikit-learn
   ```
3. Run notebooks in order (01 → 04) inside the `notebooks/` folder
4. Open `dashboards/marketplace_dashboard.pbix` in Power BI Desktop

---

## 👤 Author

**Abdelrahman Mahmoud**
NTI Data Analytics Training Program
