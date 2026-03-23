# 🚛 Logistics Intelligence Dashboard: Advanced Visualization, Insights & Operational Strategy

A 5-page interactive Power BI report built to analyze transportation and fleet operations — integrating 14 logistics datasets across trips, drivers, vehicles, fuel, maintenance, and safety to deliver executive-level insights on operational efficiency, cost control, driver performance, and financial profitability.

---

[![Power BI PBIX](https://img.shields.io/badge/Power%20BI-Download%20.pbix-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://github.com/hetav22/Powerbi-Portfolio/blob/d610b0784700da1cc44a7a343924a63e899bf75a/Logistics%20Intelligence%20Dashboard.pbix)
[![Power BI PDF](https://img.shields.io/badge/Power%20BI-View%20PDF-EC1C24?style=for-the-badge&logo=adobeacrobatreader&logoColor=white)](https://github.com/hetav22/Powerbi-Portfolio/blob/d610b0784700da1cc44a7a343924a63e899bf75a/Logistics%20Intelligence%20Dashboard.pdf)
[![Data Sources](https://img.shields.io/badge/Data-Sources-4285F4?style=for-the-badge&logo=googledrive&logoColor=white)](https://drive.google.com/drive/u/2/folders/1uDcRTD-CkiaF6yCEXfiBgXyuJ7VFaAfD)

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| 📊 Power BI Desktop | Main platform for report creation and visualization |
| 📂 Power Query | Data cleaning, transformation, and calculated field creation |
| 🧠 DAX (Data Analysis Expressions) | Advanced KPIs using CALCULATE, DIVIDE, SWITCH, VAR, MAXX |
| 🔗 Data Modeling | Star-schema relational model linking 14 datasets |
| 📁 File Format | `.pbix` for development, `.pdf` for dashboard previews |

---

## 📁 Data Source

**Source:** Multiple structured Excel datasets covering logistics and fleet operations.

14 interconnected datasets integrated in Power BI:

| Dataset | Purpose |
|---------|---------|
| Trips | Trip-level journey details — distance, duration, completion status |
| Loads | Shipment data — weight, origin, destination, revenue |
| Customers | Customer profiles — demand patterns, service performance |
| Drivers | Driver profiles — experience, assignments |
| Driver Monthly Metrics | Monthly productivity — trips completed, hours worked |
| Trucks | Fleet details — capacity, type, operational status |
| Trailers | Trailer usage and availability |
| Truck Utilization Metrics | Utilization rates and idle time per vehicle |
| Fuel Purchases | Fuel quantity, cost, and purchase date |
| Maintenance Records | Repair history, cost, and frequency per vehicle |
| Routes | Route distance and efficiency data |
| Delivery Events | Real-time delivery status — dispatched, delayed, completed |
| Safety Incidents | Accidents, DOT violations, compliance events |
| Facilities | Depot and warehouse operational data |

All tables are connected via a **star-schema** with one-to-many relationships from dimension tables (Customers, Drivers, Trucks, Routes, Date) to fact tables (Trips, Loads, Fuel, Maintenance, Safety Incidents).


---

## ✨ Features & Highlights

### 🔴 Business Problem
Transportation and logistics companies manage complex, multi-source operational data but lack a unified view to monitor performance across drivers, fleet, costs, and delivery reliability. Key questions like:
- What is the overall fleet utilization and profitability?
- Which drivers and routes are underperforming or high-risk?
- Where are operational bottlenecks causing delivery delays?
- How much do fuel and maintenance costs impact margins?

…are difficult to diagnose without integrated visual analytics.

### 🎯 Goal of the Dashboard
To deliver a 5-page Power BI report that:
- Provides executives with a real-time operational command center
- Identifies driver compliance and safety risks
- Surfaces fleet and fuel cost inefficiencies
- Enables financial deep-dive by route, destination, and time period

---

### 🧠 Key DAX Measures

| Measure | Logic |
|---------|-------|
| **Utilization Rate** | Total miles ÷ (trucks × days × 450 miles/day benchmark) |
| **Safety Score** | 100 − (incidents ÷ trips × 1000) |
| **Incident Rate** | Incidents per 100,000 miles driven |
| **On-Time Rate** | On-time deliveries ÷ total deliveries |
| **Fuel CPM** | Total fuel cost ÷ total miles |
| **Profit per Mile** | Gross profit ÷ total miles |
| **Asset Velocity** | Total trips ÷ distinct trucks |
| **Driver Rating Stars** | SWITCH on Safety Score → 1–5 star rating |
| **Repeat Customer %** | Customers with multiple loads ÷ total unique customers |
| **Turnover Rate** | Terminated drivers ÷ total drivers |

---

### 📄 Walkthrough of Dashboard Pages

#### Page 1 — Executive Command Center
**KPIs:** Total Revenue (298.62M), Total Miles (122M), Fleet Utilization (83%), Safety Score, Avg Trip Duration

Key visuals:
- **Monthly Revenue Trend (Line Chart)** – Stable revenue with minor fluctuations indicating consistent demand
- **Revenue by Region (Geographic Heatmap)** – Bubble map showing regional revenue concentration
- **Top Customer Revenue (Treemap)** – A few key customers drive a major share of total revenue — concentration risk identified
- **Fleet Health Matrix (Table)** – Vehicle make vs MPG, utilization %, and maintenance cost comparison
- **On-Time Delivery (Gauge Chart)** – Performance at 0.45 — below optimal benchmark, indicating service reliability gap

---

#### Page 2 — Operations & Driver Performance
Key visuals:
- **Delay Reason Analysis (Bar Chart)** – DOT violations (26 cases) are the leading delay cause, followed by accidents and customer complaints
- **On-Time Delivery Performance (Gauge)** – Below benchmark; route optimization needed
- **Facility Bottlenecks (Horizontal Bar)** – Certain facilities show significantly higher detention hours
- **Booking Type Revenue Split (Donut)** – Dedicated and contract bookings dominate; spot bookings are secondary
- **Load Weight Distribution (Histogram)** – Consistent load patterns; heavy outliers require special planning
- **Revenue by Segment (Line Chart)** – Automotive and Consumer Goods consistently outperform other freight segments

---

#### Page 3 — Driver Performance & Compliance
Key visuals:
- **Driver KPI Scorecard** – Revenue contribution, avg MPG, and star safety rating per driver
- **Safety Incidents by Driver (Stacked Bar)** – A small group of drivers accounts for a disproportionate share of incidents
- **Incident Type Breakdown (Treemap)** – DOT violations and accidents are the most frequent incident types
- **Monthly Performance Trend (Line Chart)** – Revenue and miles stable; MPG shows slight fluctuation
- **Incident Volume by Month (Column Chart)** – Preventable vs non-preventable incident split over time

**Key Insight:** Avg MPG across drivers is ~6.50. Preventable incidents form a significant portion of total incidents — driver training is a high-ROI intervention.

---

#### Page 4 — Fleet, Fuel & Cost Optimization
**KPIs:** Total Fuel Cost (95.59M), Maintenance Cost (5.73M), Fleet Avg MPG

Key visuals:
- **Fuel Cost vs Miles Driven (Bar + Line)** – Fuel consumption tracks directly with operational activity
- **Asset Status Breakdown (Donut)** – Majority active; portion inactive or under maintenance
- **Fleet Avg MPG (Gauge)** – Stable but limited improvement over time
- **Maintenance Cost by Category (Donut)** – Both routine and emergency repairs contribute significantly
- **Under-Utilized Assets (Table)** – Trucks with high idle days and lower revenue contribution identified
- **Monthly Asset Velocity Trend (Line Chart)** – Declining trend in recent months signals operational slowdown

---

#### Page 5 — Financial Deep-Dive
**KPIs:** Gross Profit (197.30M), Profit per Mile (₹1.62), Total Expenses (101.32M)

Key visuals:
- **Revenue vs Expenses Trend (Area Chart)** – Revenue consistently exceeds expenses across all months
- **Profitability by Destination (Bubble Map)** – High- and low-margin routes identified geographically
- **Monthly Financial Scorecard (Table)** – Month-by-month breakdown of revenue, fuel, maintenance, gross profit, and profit per mile
- **Fuel vs Maintenance Cost Split (Donut)** – Fuel dominates at 95.59M vs maintenance at 5.73M

---

### 📈 Business Impact & Insights

- **Revenue & Profitability:** 298.62M revenue, 197.30M gross profit, 1.62 profit per mile — financially healthy with controlled expenses
- **Fleet Efficiency:** 83% utilization rate; several trucks identified with high idle days — reallocation opportunity
- **Fuel Cost Control:** Fuel is the single largest cost driver (95.59M) — route optimization and MPG improvement are highest-ROI interventions
- **Delivery Reliability:** On-time rate at 0.45 — below benchmark; DOT violations and facility bottlenecks are primary root causes
- **Driver Safety:** Preventable incidents are significant — targeted compliance training can reduce incidents and associated fines
- **Customer Concentration:** A few customers drive majority revenue — diversification is a strategic priority

---

## 📸 Screenshots

<img width="1455" height="830" alt="image" src="https://github.com/user-attachments/assets/01de51e4-2b9f-4061-a1ed-6375cf547abc" />


---

## ⚠️ Limitations

- Analysis is historical only — no predictive modeling or forecasting included
- External factors (fuel price volatility, market conditions) not incorporated
- Dataset scope limited to available operational variables; qualitative factors not captured

---

[![Back to Main](https://img.shields.io/badge/←%20Back%20to-Main%20Portfolio-2D333B?style=for-the-badge)](../../tree/main)

---
## 🔗 Navigation

Each project in this portfolio is in its own branch. Switch to the relevant branch to explore files, `.pbix`, and dashboard previews.
