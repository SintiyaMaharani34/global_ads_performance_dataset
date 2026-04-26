# 📊 Global Ads Performance Analysis

## 📌 Project Overview

This project analyzes global digital advertising performance across multiple platforms including Google Ads, Meta Ads, and TikTok Ads. The goal is to evaluate campaign effectiveness, identify high-performing segments, and provide actionable business insights.

The analysis follows a complete data analytics workflow:

* Data Cleaning using Python
* Exploratory Data Analysis (EDA) using PostgreSQL
* Data Visualization and Dashboarding using Power BI

---

## 🎯 Objectives

* Identify the most profitable advertising platform
* Analyze performance across different industries
* Evaluate marketing efficiency using key metrics (ROAS, CPC, CTR)
* Understand monthly trends in ad performance
* Provide recommendations to optimize marketing budget allocation

---

## 🗂️ Dataset

* Source: Kaggle – Global Ads Performance Dataset
* Features include:

  * Platform (Google, Meta, TikTok)
  * Campaign Type
  * Industry
  * Country
  * Impressions, Clicks, Conversions
  * Ad Spend, Revenue
  * CTR, CPC, CPA, ROAS

---

## ⚙️ Tools & Technologies

* Python (Pandas) → Data Cleaning
* PostgreSQL → Data Analysis (EDA)
* Power BI → Dashboard & Visualization

---

## 🧹 Data Cleaning (Python)

Steps performed:

* Handled missing values
* Standardized column formats
* Converted dataset delimiter to CSV format
* Removed irrelevant or incomplete records

---

## 🗄️ Data Analysis (SQL)

Performed using PostgreSQL:

* Platform performance (ROAS, Revenue, Spend)
* Industry-level profitability analysis
* Cost efficiency analysis (CPC)
* Monthly trend analysis using date functions
* Campaign and country-level insights

Example Query:

```sql
SELECT 
    platform,
    SUM(ad_spend) AS total_spend,
    SUM(revenue) AS total_revenue,
    ROUND(
        (SUM(revenue) / NULLIF(SUM(ad_spend), 0))::numeric
    , 2) AS roas
FROM ads_data
GROUP BY platform
ORDER BY roas DESC;
```

---

## 📊 Dashboard (Power BI)

The interactive dashboard includes:

* KPI Cards (Total Spend, Revenue, ROAS, CTR)
* Platform Performance Comparison
* Industry Analysis
* Monthly Trend (Revenue & Spend)
* Country Performance
* Campaign Type Analysis

---

## 🔍 Key Insights

* TikTok Ads generated the highest ROAS, indicating strong return efficiency
* Google Ads had the highest spend but lower efficiency compared to other platforms
* Certain industries significantly outperform others in profitability
* Clear seasonal trends observed in monthly performance
* CPC varies significantly across platforms, impacting cost efficiency

---

## 💡 Recommendations

* Allocate more budget to high-ROAS platforms (e.g., TikTok Ads)
* Optimize underperforming platforms with high spend but low returns
* Focus marketing efforts on high-performing industries
* Adjust campaign strategies based on seasonal trends
* Continuously monitor CPC and CTR to improve efficiency

---

## 🚀 Project Structure

```
global_ads_performance/
│
├── data/
│   └── ads_clean.csv
│
├── python/
│   └── data_cleaning.ipynb
│
├── sql/
│   └── analysis_queries.sql
│
├── dashboard/
│   └── powerbi_dashboard.pbix
│
└── README.md
```

---

## 📌 Conclusion

This project demonstrates an end-to-end data analytics workflow, transforming raw marketing data into actionable insights. By combining SQL-based analysis with interactive visualization, the project provides valuable recommendations for optimizing advertising strategies.

---

## 👩‍💻 Author

**Sintiya Maharani**
Aspiring Data Analyst | SQL | Python | Power BI
