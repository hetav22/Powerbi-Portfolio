# 🛍️ Understanding Retail Growth: A Data-Driven Look at Sales and Consumer Behavior

A capstone analytics project analyzing over 1 million retail transactions to uncover key revenue drivers, customer behavior patterns, discount effectiveness, and seasonal demand trends — combining Python-based statistical analysis with interactive Power BI dashboards.

---

[![Power BI PBIX](https://img.shields.io/badge/Power%20BI-Download%20.pbix-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](your-pbix-link)
[![Power BI PDF](https://img.shields.io/badge/Power%20BI-View%20PDF-EC1C24?style=for-the-badge&logo=adobeacrobatreader&logoColor=white)](your-pdf-link)
[![Data Sources](https://img.shields.io/badge/Data-Sources-4285F4?style=for-the-badge&logo=googledrive&logoColor=white)](https://drive.google.com/drive/u/2/folders/1gBdAR_grfNnnqXVEeU44Q1sJT06i8a_M)

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| 🐍 Python | Statistical analysis — ANOVA, t-test, RFM segmentation, seasonality decomposition |
| 📊 Power BI Desktop | Interactive dashboard creation and visualization |
| 📂 Power Query | Data transformation and preparation |
| 🧠 DAX | Calculated KPIs and measures |
| 📦 Libraries | `pandas`, `numpy`, `scipy`, `statsmodels`, `matplotlib`, `seaborn` |
| 📁 File Format | `.pbix` for dashboard, `.ipynb` for Python analysis, `.png` for previews |

---

## 📁 Data Source

**Source:** Kaggle — Large Retail Dataset for Exploratory Data Analysis (EDA)

The dataset contains transaction-level retail data covering:

- **Sales & Revenue** – Transaction date, quantity, unit price, gross and net revenue
- **Discounts** – Discount applied per transaction, categorized into Very Low / Low / Medium levels
- **Products** – Product categories: Clothing, Electronics, Furniture, Groceries, Toys
- **Customers** – Customer IDs, transaction count (new vs repeat), demographics
- **Geography** – State-level regional data
- **Time** – Transaction dates, month, quarter, year for time-series analysis

**Sample size used for analysis:** 1M+ transactions (120,000 sampled for ANOVA testing)

> Raw dataset files are hosted externally due to size.
> [Download Dataset (Google Drive)](your-drive-link)

---

## ✨ Features & Highlights

### 🔴 Business Problem
Retailers generate massive volumes of transactional data but often lack structured methods to answer:
- Do discounts actually increase revenue, or just erode margins?
- Are repeat customers more valuable than new ones?
- Are there significant seasonal patterns that should drive inventory and promotional planning?
- Which customer segments are at risk of churning?

### 🎯 Goal of the Dashboard
To deliver a 2-page Power BI dashboard — backed by rigorous Python statistical testing — that:
- Identifies key revenue drivers across product categories, discount levels, and regions
- Segments customers using RFM analysis to support targeted retention strategies
- Surfaces seasonal and monthly demand patterns for operational planning
- Quantifies retention risk across new vs repeat customer groups

---

### 🔬 Statistical Analysis (Python)

#### 1. Discount Impact on Sales — Two-Way ANOVA + Tukey HSD

**Test:** Two-Way ANOVA on Net Revenue ~ Discount Level × Product Category

| Source | Result | Decision |
|--------|--------|----------|
| Discount Level | Significant (p < 0.05) | Reject H0 — discount level significantly affects net revenue |
| Product Category | Not Significant | Retain H0 — categories perform similarly |
| Discount × Category Interaction | Not Significant | Discounts have a universal effect across all product categories |

**Tukey HSD Post-Hoc:** All pairwise comparisons (Very Low vs Low vs Medium) are statistically significant. As discount level increases, average net revenue per transaction **decreases** — confirming that heavier discounts hurt margins without proportionally boosting volume.

---

#### 2. Repeat vs New Customers — Independent Samples t-Test

**Test:** t-Test on Net Revenue between Repeat and New customers

| Statistic | p-value | Decision |
|-----------|---------|----------|
| 0.879 | 0.379 | Fail to reject H0 — no significant revenue difference between customer types |

Average transaction value is not significantly different between new and repeat customers. However, repeat customers show lower churn risk and contribute the majority of total revenue through higher purchase frequency.

---

#### 3. Seasonal Trends — One-Way ANOVA + Decomposition

**Test:** One-Way ANOVA on Net Revenue across 12 months

| F-statistic | p-value | Decision |
|-------------|---------|----------|
| — | 0.002132 | Reject H0 — monthly net revenue varies significantly across the year |

Seasonality decomposition (additive model, period=12) confirms a recurring seasonal component in sales, with identifiable peak and low-demand months.

---

### 📄 Walkthrough of Dashboard Pages

#### Page 1 — Revenue Drivers & Demand Analysis
**KPI:** Total Revenue (1.88bn)

Key visuals:
- **Revenue by Product Category (Horizontal Bar Chart)** – Balanced contribution across Clothing, Electronics, Furniture, Groceries, and Toys — no single category dominates
- **Discount vs Revenue (Bubble/Scatter Chart)** – Revenue increases from Very Low to Medium discount levels, but growth is not proportional — heavy discounting provides diminishing returns
- **Seasonality Strength (Quarter-wise Matrix Table)** – Highlights seasonal revenue patterns by product category across all four quarters
- **Monthly Demand Evolution (Line Chart)** – Tracks revenue month-by-month; identifies consistent peak and low-demand periods

**Key Insights:**
- Revenue is diversified across categories, reducing business risk
- Moderate discounts outperform heavy discounting — margin discipline is critical
- Seasonal patterns are statistically significant and should drive inventory and promotional planning

---

#### Page 2 — Customer Analytics: Retention & Segmentation Strategy
**KPIs:** Total Customers (1M), Average Transaction Value (₹1.88K)

Key visuals:
- **Retention Risk Index (Bar Chart)** – New customers have significantly higher churn risk vs repeat customers
- **Revenue by Customer Type (Bar Chart)** – Repeat customers contribute the majority of total revenue
- **RFM Segment Behavioral Profile (Table)** – Detailed Recency, Frequency, and Monetary values for Champions, Loyal Customers, At-Risk, and New Customer segments
- **Segment Share of Total Customers (Donut Chart)** – Visual distribution of customers across all RFM segments

**Key Insights:**
- Champions and Loyal Customers generate the highest monetary value and purchase frequency
- A significant share of customers fall in "Need Attention" and "New Customer" segments — engagement strategies needed
- New customers have higher churn risk; converting them to repeat buyers is the highest-ROI retention strategy

---

### 📈 Business Impact & Insights

- **Discount Strategy:** Moderate discounting (not heavy) is optimal — verified statistically. Excessive discounts reduce net revenue per transaction without significantly increasing volume.
- **Customer Retention:** Repeat customers drive majority revenue despite no statistical difference in individual transaction value — frequency is the key differentiator.
- **Seasonal Planning:** Monthly demand fluctuations are statistically significant — inventory, staffing, and promotions should align with identified peak months.
- **RFM Segmentation:** Enables precise marketing budget allocation — invest in Champions and Loyal Customers, re-engage At-Risk segments, convert New Customers.
- **Regional Performance:** Revenue is stable across states — no over-reliance on a specific geography.

---

## 📸 Screenshot

<img width="1428" height="786" alt="Screenshot 2026-03-23 184740" src="https://github.com/user-attachments/assets/a1268bd0-b196-4930-8e16-c556fc479c6e" />


---

## ⚠️ Limitations

- Based on secondary data from Kaggle — findings may not generalize directly to real retail businesses
- Dataset uses synthetic/uniform distributions which may understate real-world variance
- Analysis is descriptive and diagnostic — no predictive modeling included
- Qualitative factors (brand perception, customer satisfaction) are not captured

---

[![Back to Main](https://img.shields.io/badge/←%20Back%20to-Main%20Portfolio-2D333B?style=for-the-badge)](../../tree/main)

---
