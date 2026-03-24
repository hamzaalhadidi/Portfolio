
# 🛍️ Customer Shopping Behavior Analysis

## 📌 Overview
An end-to-end data analysis project exploring customer shopping behavior using transactional data from a retail store across 50 US states. The goal is to uncover insights into spending patterns, customer segments, and product preferences to support business decisions.

---

## 📊 Dataset
- **Rows:** 3,900 transactions
- **Columns:** 18 features (demographics, purchase details, shopping behavior)
- **Missing Data:** 37 values in `review_rating` — filled using category median

---

## 🔄 Workflow

### 1️⃣ Python — Data Cleaning & Preparation
- Handled missing values, dropped redundant columns, standardized column names to `snake_case`
- Feature engineering: `age_group`, `purchases_frequency_days`
- Exported cleaned data to **SQL Server** via `SQLAlchemy`

### 2️⃣ SQL — Business Analysis
13 queries answering key business questions using `CTE`, `Window Functions`, `GROUP BY`, and `CASE WHEN`

### 3️⃣ Power BI — Interactive Dashboard
4-page dashboard with 12+ DAX measures, conditional formatting, and cross-page slicers

---

## 📈 Key Findings
| Finding | Value |
|---------|-------|
| Total Revenue | $233,081 |
| Loyal Customers | 80% of customer base |
| Subscription Rate | Only 27% |
| Top Revenue Age Group | Middle-Aged — $67,711 |
| Highest Rated Product | Gloves — 3.86 |
| Top State | Montana — $5,784 |

---

## 🛠️ Tools
**Python** • **SQL Server** • **Power BI** • **DAX** • **SQLAlchemy** • **Pandas**
