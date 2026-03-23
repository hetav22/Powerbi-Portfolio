# 🛒 Optimizing Retail Operations: Advanced Insights from Power BI Dashboard Analytics

An interactive, multi-page Power BI report built to analyze retail business performance across sales, customers, products, and time — enabling data-driven decisions through visual KPIs, drill-downs, and cross-filtering.

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| 📊 Power BI Desktop | Main platform for report creation and visualization |
| 📂 Power Query | Data cleaning, transformation, and shaping |
| 🧠 DAX (Data Analysis Expressions) | Calculated measures, KPIs, and time intelligence |
| 🔗 Data Modeling | Star schema linking Sales (fact) to Products, Stores, Customers, and Dates (dimensions) |
| 📁 File Format | `.pbix`,`.pbit` for development, `.png` for dashboard previews |

---

## 📁 Data Source

**Source:** Multiple Excel files loaded into Power BI Desktop.

The dataset covers a retail business with the following tables:

- **Sales** – Core transactional data: date, store, product, quantity, and amount
- **Products** – Product IDs, names, categories, sub-categories, brands, cost and selling price
- **Stores** – Store IDs, names, cities, regions, and managers
- **Customers** – Customer IDs, demographics (age group, gender, city), and loyalty/activity status
- **Dates** – Calendar dimension with year, quarter, month, weekday/weekend flags for time intelligence

Relationships are established via `ProductID`, `StoreID`, `CustomerID`, and `Date` keys in a one-to-many structure from dimension tables to the Sales fact table.

---

## ✨ Features & Highlights

### 🔴 Business Problem
Retail businesses generate large volumes of transactional data across stores, products, and customers — but lack a quick, intuitive way to diagnose performance issues or spot opportunities. Key questions like:
- Which regions and product categories are most profitable?
- Which customer segments drive the most revenue?
- Are discounts actually boosting sales?
- How does performance shift across time and seasons?

…are hard to answer from raw spreadsheets alone.

### 🎯 Goal of the Dashboard
To deliver a 5-page interactive Power BI report that:
- Converts raw retail data into actionable visual insights
- Supports decisions across sales, marketing, inventory, and customer management
- Enables drill-down exploration by time, region, category, and customer segment

---

### 📄 Walkthrough of Key Pages

#### Page 1 — Sales & Revenue Overview
**KPIs:** Total Sales (230.47M), Profit Margin (24.7%), Transactions (500K), Avg Sale (₹460.93)

Key visuals:
- **Revenue by Region (Donut Chart)** – North and West lead; East and Central lag, pointing to marketing and distribution gaps
- **Sales Trend Over Time (Line Chart)** – Tracks monthly performance; peaks align with seasonal demand
- **Payment Mode (Donut Chart)** – UPI leads, followed by Cash; card and wallet usage is low
- **Region-Wise Sales Breakdown (Bar Chart)** – Compares profit across geographic zones

---

#### Page 2 — Customer Analysis
**KPIs:** Total Customers (15K), Loyalty vs Non-loyalty split, Avg Revenue per Customer & Store

Key visuals:
- **Sales by Age Group (Bar Chart)** – Ages 21–60 contribute the majority of revenue
- **Members Comparison (Bar Chart)** – Loyalty vs non-loyalty member performance
- **Revenue by Gender (Donut Chart)** – Balanced across genders; "Other" category also contributes
- **City-Wise Customer Sales (Map)** – Urban centres dominate; some cities show strong growth potential

---

#### Page 3 — Product Performance
**KPIs:** Quantity Sold (884K units), Avg Selling Price (₹266.67), Revenue (230.47M), Profit (56.93M)

Key visuals:
- **Sales & Profit Margin % by Category (Bar + Line)** – Personal Care, Snacks, and Household items lead sales; Beverages and Staples have lower margins
- **Profit by Category (Bar Chart)** – Absolute profit comparison; Bakery underperforms relative to sales
- **Top Products by Revenue (Table)** – Shampoos, cleaning products, and grocery staples top the list
- **Quantity Sold by Brand (Bar Chart)** – Britannia, Mother Dairy, and Modern Bakery stand out in volume

---

#### Page 4 — Time Series & Seasonality
**KPIs:** Total Sales, YTD Profit, Avg Daily Sales (315K)

Key visuals:
- **Monthly Sales Comparison (Bar Chart)** – Consistent performance with identifiable slow months
- **Quarterly Performance (Donut Chart)** – Q4 slightly leads, likely driven by festive season demand
- **Year-over-Year Comparison (Stacked Bar)** – 2024 vs 2023 monthly comparison to track growth
- **Weekday vs Weekend (Bar Chart)** – Weekdays significantly outperform weekends

---

#### Page 5 — Advanced Insights
**KPIs:** Transaction Count, Avg Discount % (0.02%), Profit Margin (24.7%), Revenue per Transaction

Key visuals:
- **Discount % Impact on Sales (Scatter Plot)** – High discounts show minimal effect on volume; pricing discipline is effective
- **Profit by Payment Mode (Bar Chart)** – UPI and Cash generate the highest profit
- **Customer Segment Profitability (Bar Chart)** – Loyalty members and mid-age segments (31–50) are most profitable

---

### 📈 Business Impact & Insights

- **Sales Strategy:** Moderate discounting outperforms heavy discounting — price discipline maintained at 24.7% margin
- **Customer Retention:** Loyalty program has room to grow; non-loyalty members still outnumber loyalty members
- **Regional Focus:** North and West are strong markets; East and Central need targeted interventions
- **Inventory Planning:** Weekday demand patterns and Q4 seasonality can directly guide stock and staffing decisions
- **Payment Optimization:** UPI and Cash dominate profit — digital-first checkout improvements are justified

---

## 📸 Screenshot

<img width="1276" height="717" alt="image" src="https://github.com/user-attachments/assets/2d03cf24-5022-4b32-9239-658427ce931b" />

---


