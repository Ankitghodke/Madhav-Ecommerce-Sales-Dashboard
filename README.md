# 🛒 Madhav E-Commerce Sales Dashboard
Power BI · Data Modeling · DAX · Business Intelligence

---

## 📌 Overview

E-commerce businesses generate a lot of order data but rarely have a clear view of where profit is actually coming from. This dashboard analyzes 500 orders across 19 Indian states to break down revenue by category, track monthly profit trends, and identify which segments are losing money and when.

Total sales: ₹4.38L across 336 unique customers and 25 cities.

**Tech stack:**
- Power BI Desktop — dashboard design, DAX measures, data modeling
- Power Query — data transformation, cleaning, reshaping
- Data source — Orders.csv + Details.csv (relational datasets)

---

## 🏗️ How it works
```
Orders.csv + Details.csv (Raw Data)
        ↓
Power Query (Data Cleaning + Transformation)
        ↓
Power BI Data Model (Relationship via Order ID)
        ↓
DAX Measures (KPIs + Calculated Columns)
        ↓
Interactive Executive Dashboard
```

---

## 📊 Dataset

| Metric | Value |
|--------|-------|
| Total orders | 500 |
| Total line items | 1,500 |
| Total sales amount | ₹4,37,771 |
| Total profit | ₹36,963 |
| Total quantity sold | 5,615 units |
| Avg order value | ₹291.85 |
| Profit margin | 8.44% |
| States covered | 19 |
| Cities covered | 25 |
| Unique customers | 336 |
| Product categories | 3 (Electronics, Clothing, Furniture) |
| Payment modes | 5 (COD, UPI, Debit Card, Credit Card, EMI) |

---

## 🧠 Analysis

**🔹 Data modeling**
- Merged 2 relational datasets (Orders + Details) via Order ID as relational key
- Built cross-dataset relationships for combined analysis
- Created calculated columns for Quarter, Month, and category-level aggregations

**🔹 DAX measures**
- Total Revenue, Total Profit, Total Quantity — real-time KPI tracking
- Avg Order Value calculated across 1,500 line items
- Quarterly performance filters (Q1–Q4) for trend comparison
- Profit margin at category and sub-category level

---

## 📈 Key findings

| Finding | Numbers | Note |
|---------|---------|------|
| Top revenue category | Electronics — ₹1.66L (38%) | Leads revenue despite lower volume |
| Top quantity category | Clothing — 3,516 units (62.6%) | High volume, lower revenue per unit |
| Best profit month | November — ₹10,253 | Pre-holiday demand spike |
| Loss months | May, July, September, December | 4 out of 12 months in the red |
| Top state | Maharashtra — ₹1.02L | 23.4% of total revenue alone |
| Dominant payment mode | COD — 684 transactions (45.6%) | Digital payment adoption is low |
| Top customer | Harivansh — ₹9,902 | Highest individual revenue contributor |

**🔹 Sub-category profit leaders**

| Sub-category | Profit |
|-------------|--------|
| Printers | ₹8,606 |
| Bookcases | ₹6,516 |
| Saree | ₹4,057 |
| Accessories | ₹3,353 |
| Tables | ₹3,139 |

**🔹 State-wise revenue**

| State | Revenue |
|-------|---------|
| Maharashtra | ₹1,02,498 |
| Madhya Pradesh | ₹87,463 |
| Uttar Pradesh | ₹38,362 |
| Delhi | ₹22,957 |
| Rajasthan | ₹22,334 |

---

## 📊 Dashboard features

KPI cards: Total Sales (₹4.38L), Total Profit (₹36,963), Total Quantity (5,615 units), Avg Order Value (₹291.85)

Visuals included:
- Profit and loss by month (12-month trend)
- Revenue by state (top 5 comparison)
- Sales by category and sub-category
- Customer-wise revenue breakdown
- Payment mode distribution (pie chart)
- Quarterly filter (Q1, Q2, Q3, Q4)

---

## 📂 File structure
```
Madhav-Store-Sales-Dashboard/
├── madhavstores.pbix
├── Orders__1_.csv
├── Details.csv
└── msd.PNG
```

---

## 🚀 How to run

1. Download `Orders__1_.csv` and `Details.csv`
2. Open `madhavstores.pbix` in Power BI Desktop
3. Explore the dashboard using quarter filters and category slicers
4. All relationships and DAX measures are pre-built — no setup required

---

## 📸 Dashboard preview

![Dashboard](msd.PNG)

---

## 🎯 Conclusions

The most useful tension in this dataset is between Clothing and Electronics. Clothing accounts for 62.6% of units sold but Electronics drives 38% of revenue — meaning the business is moving a lot of low-margin apparel while a smaller number of electronics orders carry the revenue. That gap is worth watching as inventory decisions get made.

The 4 loss-making months (May, July, September, December) are scattered enough that it's probably not one seasonal pattern — it's multiple. December being a loss month is the most surprising given it's typically a strong retail period. That alone is worth digging into.

COD sitting at 45.6% of transactions is a cash flow and logistics cost that compounds quietly. Every COD order that gets returned costs more than a prepaid one. The data doesn't show return rates here, but if they're available, that's the next analysis worth running.

Maharashtra contributing nearly a quarter of total revenue from one state is both an asset and a concentration risk. The drop-off to Madhya Pradesh at ₹87K and then to UP at ₹38K is steep.
