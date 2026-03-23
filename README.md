# 📱 Analyzing Effectiveness of Influencer Marketing

An interactive Power BI report built to evaluate the financial performance of a fashion brand's influencer marketing program — analyzing ROI, revenue vs cost, customer lifetime value, and audience profiling across influencers, campaigns, and channels.

---

[![Power BI PBIX](https://img.shields.io/badge/Power%20BI-Download%20.pbix-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://github.com/hetav22/Powerbi-Portfolio/blob/cfee25b3820eecb99fde51fe84d22d820d380936/Influencer%20Marketing%20Effectiveness.pbix)
[![Power BI PDF](https://img.shields.io/badge/Power%20BI-View%20PDF-EC1C24?style=for-the-badge&logo=adobeacrobatreader&logoColor=white)](https://github.com/hetav22/Powerbi-Portfolio/blob/cfee25b3820eecb99fde51fe84d22d820d380936/Influencer%20Marketing%20Effectiveness.pdf)
[![Data Sources](https://img.shields.io/badge/Data-Sources-4285F4?style=for-the-badge&logo=googledrive&logoColor=white)](https://drive.google.com/drive/u/2/folders/1RPskOG6I6CBFGLh3t3lZgim3pa3WHvCU)

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| 📊 Power BI Desktop | Main platform for report creation and visualization |
| 📂 Power Query | Data cleaning, transformation, and preparation |
| 🧠 DAX (Data Analysis Expressions) | Calculated measures, KPIs, ROI and LTV metrics |
| 🔗 Data Modeling | Relationships across campaign, influencer, product, and customer tables |
| 📁 File Format | `.pbix` for development, `.pdf` for dashboard previews |

---

## 📁 Data Source

**Source:** Kaggle — Synthetic influencer marketing campaign dataset for the fashion industry

> Dataset link: [Influencer Marketing Campaign Analysis – Kaggle](https://www.kaggle.com/datasets/divyamehulmak/influencer-marketing-campaign-analysis-power-bi)

The dataset covers multiple campaigns from 2024–2025 and includes:

- **Campaign Data** – Campaign IDs, start/end dates, budget, cost, revenue, conversion rate targets
- **Influencer Profiles** – Influencer IDs, names, tier levels, channel/platform
- **Order Data** – Total amount, average order value (AOV), lifetime value (LTV)
- **Customer Demographics** – Age group, gender, city/location, new vs returning status

Data types include categorical (IDs, names), numerical (revenue, cost, budget), dates, and percentage metrics.


---

## ✨ Features & Highlights

### 🔴 Business Problem
Brands investing in influencer marketing often lack clarity on which influencers, campaigns, and channels actually deliver returns. Key questions like:
- What is the overall ROI of the influencer program?
- Which influencers generate the highest revenue and profitability?
- Do different channels affect how much customers spend?
- Which customer segments are most loyal and valuable?

…are difficult to answer without a structured analytical approach.

### 🎯 Goal of the Dashboard
To deliver an interactive Power BI report that:
- Evaluates financial performance of the influencer marketing program
- Identifies high-ROI and high-LTV influencers worth long-term investment
- Profiles the customer base to support targeted marketing decisions
- Surfaces campaign-level differences in order value and customer lifetime value

---

### 📄 Walkthrough of Key Pages

#### Page 1 — Influencer Effectiveness
**KPIs:** Total Revenue (~352.85M), Average ROI (~296₹)

Key visuals:
- **ROI Line Chart** – A small group of influencers deliver extremely high ROI; most others taper off sharply — classic power-law distribution
- **Conversions Treemap** – BeautyBuzz, SustainableChic, and VintageFinds dominate total conversions
- **Revenue vs Cost Bar Chart** – BeautyBuzz and SustainableChic show revenue bars far above their cost bars, confirming strong profitability
- **Detailed Stats Table** – BeautyBuzz leads in total revenue (~81M); smaller influencers like BudgetStylist show higher ROI efficiency but lower absolute reach

**Key Insight:** There's a clear trade-off — some influencers are revenue giants but expensive; others are cheap and highly efficient but limited in scale.

---

#### Page 2 — Influencer Value Analysis
Key visuals:
- **Influencer vs Customer LTV (Bar Chart)** – MinimalistMan and BudgetStylist bring in customers with the highest lifetime value; StyleSensei and VintageFinds are at the lower end
- **Influencer vs AOV (Bar Chart)** – BudgetStylist, MinimalistMan, and TheStreetLook drive the highest average order value per transaction

**Key Insight:** Certain influencers consistently attract customers who spend more per order and return more often — these are the highest-priority partnerships.

---

#### Page 3 — Customer Profile & Segmentation
Key visuals:
- **Top Customer Profiles Table** – Highest LTV customers are mainly 45+, often male, preferring luxury, formal, or streetwear styles
- **Age Group Bar Chart** – 25–34 is the dominant segment, followed by 18–24 and 35–44
- **Gender Donut Chart** – Male, female, and "other" customers are nearly evenly split (~1/3 each)
- **New vs Returning Customers Pie Chart** – Returning customers make up the vast majority, indicating strong loyalty
- **Location Map** – Customers cluster around major Indian cities in the north, west, and south

**Key Insight:** Core audience is 18–34, urban, gender-balanced, and highly loyal. Older customers (45+) are fewer but premium in value.

---

### 📊 Statistical Analysis (ANOVA Results)

One-Way ANOVA tests were run to determine whether channels, influencers, and campaigns significantly affect customer spending:

| Test | Result |
|------|--------|
| Total Amount vs Channel | p ≈ 0 → Significant. Instagram delivers the highest average order value. |
| Total Amount vs Influencer ID | p ≈ 0 → Significant. INF003, INF019, INF020, INF004 drive higher basket sizes. |
| Total Amount vs Campaign ID | p ≈ 0 → Significant. CMP006, CMP009, CMP001 average ~₹4,200–4,250 vs overall avg of ~₹3,529. |
| LTV & AOV vs Campaign ID | p ≈ 0 → Significant. CMP006, CMP001, CMP007, CMP009 show higher LTV and AOV. |

All four null hypotheses rejected — influencer choice, campaign structure, and channel all significantly impact customer spending and lifetime value.

---

### 📈 Business Impact & Insights

- **Budget Allocation:** Concentrate spend on high-ROI influencers (BeautyBuzz, SustainableChic) and top campaigns (CMP006, CMP001, CMP009); exit or renegotiate low-performers
- **Channel Strategy:** Instagram is the primary performance channel for revenue and AOV; TikTok and YouTube better suited for awareness
- **Customer Retention:** Large base of returning customers — loyalty and personalization programs are justified investments
- **Premium Targeting:** Older, high-LTV customers (45+) should be targeted with luxury and formal ranges; 18–34 segment needs aspirational but accessible positioning
- **Discounting:** Basket size differences are driven by influencer and campaign quality, not heavy discounting — price discipline should be maintained

---

## 📸 Screenshot

<img width="1148" height="642" alt="image" src="https://github.com/user-attachments/assets/be00964f-b98b-4002-8d6e-1e18b302c477" />


---

## ⚠️ Limitations

- Dataset is synthetic — findings may not generalize directly to real campaigns
- Short time window (2024–2025) limits long-term trend analysis
- TikTok inclusion is inconsistent given its ban in India during this period

---

[![Back to Main](https://img.shields.io/badge/←%20Back%20to-Main%20Portfolio-2D333B?style=for-the-badge)](../../tree/main)

---
