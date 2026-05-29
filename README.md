#  Customer Shopping Behaviour Analysis

Analyzed 3,900 retail transactions to uncover spending patterns, product preferences, customer segments, and subscription behavior using **Python**, **PostgreSQL**, and **Power BI**.

---

##  Project Overview

This end-to-end data analytics project covers the full pipeline — from raw data cleaning to SQL-based business analysis and an interactive Power BI dashboard. The goal is to extract actionable insights that can guide strategic retail decisions around marketing, discounts, product positioning, and customer retention.

---

##  Dataset

| Property | Detail |
|---|---|
| Total Records | 3,900 rows |
| Total Features | 18 columns |
| Missing Data | 37 null values in `Review Rating` |

**Key columns:**
- **Demographics:** Age, Gender, Location, Subscription Status
- **Purchase Details:** Item Purchased, Category, Purchase Amount (USD), Season, Size, Color
- **Behaviour Metrics:** Discount Applied, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type, Payment Method

---

##  Tech Stack

| Tool | Purpose |
|---|---|
| Python (Pandas, NumPy) | Data cleaning & feature engineering |
| PostgreSQL | Business query analysis |
| Power BI | Interactive dashboard |

---

##  Project Workflow

### 1. Data Cleaning & EDA (Python)
- Loaded dataset using `pandas`; explored structure with `df.info()` and `.describe()`
- Imputed 37 missing `Review Rating` values using **median per product category**
- Renamed columns to **snake_case** for consistency
- **Feature Engineering:**
  - Created `age_group` column by binning customer ages
  - Created `purchase_frequency_days` from purchase frequency data
- Checked and removed redundant column (`promo_code_used` was a duplicate of `discount_applied`)
- Loaded cleaned DataFrame into **PostgreSQL** for SQL analysis

---

### 2. SQL Business Analysis (PostgreSQL)

10 business questions answered using structured queries:

| # | Analysis | Key Finding |
|---|---|---|
| 1 | Revenue by Gender | Male: $157,890 / Female: $75,191 |
| 2 | High-Spending Discount Users | 839 customers used discounts yet spent above average |
| 3 | Top 5 Products by Rating | Gloves (3.86), Sandals (3.84), Boots (3.82) |
| 4 | Shipping Type Comparison | Express avg: $60.48 / Standard avg: $58.46 |
| 5 | Subscribers vs Non-Subscribers | Avg spend nearly equal (~$59.5 vs ~$59.9) |
| 6 | Discount-Dependent Products | Hat (50%), Sneakers (49.66%), Coat (49.07%) |
| 7 | Customer Segmentation | Loyal: 3116 / Returning: 701 / New: 83 |
| 8 | Top 3 Products per Category | Jewelry, Blouse, Sandals, Jacket lead their categories |
| 9 | Repeat Buyers & Subscriptions | Non-subscribers still dominate repeat purchases (2518 vs 958) |
| 10 | Revenue by Age Group | Young Adults lead at $62,143 |

---

### 3. Power BI Dashboard

Built an interactive **Customer Behaviour Dashboard** with:
- KPI cards: Total Customers (4K), Avg Purchase Amount ($59.76), Avg Review Rating (3.75)
- Revenue & Sales by Category (bar charts)
- Revenue & Sales by Age Group (horizontal bar charts)
- Subscription status breakdown (donut chart — 73% non-subscribers)
- Slicers: Subscription Status, Gender, Category, Shipping Type

---

##  Business Recommendations

- **Boost Subscriptions** — Promote exclusive subscriber-only benefits; current subscriber base is only 27%
- **Loyalty Programs** — Reward returning buyers to move them into the Loyal segment
- **Review Discount Strategy** — Products like Hats and Sneakers have ~50% discount rates; balance sales boost with margin control
- **Product Campaigns** — Highlight top-rated products (Gloves, Sandals, Boots) in marketing
- **Targeted Marketing** — Focus on Young Adults and Express-shipping users who show higher spend

---

##  Repository Structure

```
├── data/
│   └── customer_shopping_data.csv        # Raw dataset
├── notebooks/
│   └── eda_cleaning.ipynb                # Python EDA and cleaning
├── sql/
│   └── business_queries.sql              # All 10 PostgreSQL queries
├── dashboard/
│   └── customer_behaviour_dashboard.pbix # Power BI dashboard file
├── reports/
│   └── Customer_Shopping_Behaviour_Analysis.pdf
└── README.md
```

---

##  How to Run

1. **Python Analysis**
   ```bash
   pip install pandas numpy sqlalchemy psycopg2
   jupyter notebook notebooks/eda_cleaning.ipynb
   ```

2. **PostgreSQL**
   - Create a database and import the cleaned CSV
   - Run queries from `sql/business_queries.sql`

3. **Power BI**
   - Open `dashboard/customer_behaviour_dashboard.pbix` in Power BI Desktop
   - Reconnect data source if prompted

---

##  Connect

**Anshu Singh**
- 🔗 [LinkedIn](https://linkedin.com/in/anshusingh11060)
- 💻 [GitHub](https://github.com/anshu11060)
- 📧 anshusingh11060@gmail.com
