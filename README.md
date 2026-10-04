# 🛒 Blinkit Grocery Sales Analysis – Power BI Dashboard

An interactive Power BI dashboard that analyzes **$1.20M in sales** across **8,523 items**, **16 product categories** and **10 outlets** in Tier 1, 2 and 3 cities for Blinkit, India's last-minute grocery delivery app.

![Dashboard Preview](dashboard.png)

---

## 📌 Project Objective
Analyze Blinkit's sales performance, customer preferences and outlet performance to find the key revenue drivers and opportunities for growth.

## 📂 Dataset
- **Source:** BlinkIT Grocery Data (Excel)
- **Records:** 8,523 rows × 12 columns
- **Key fields:** Item Type, Item Fat Content, Item Visibility, Item Weight, Outlet Identifier, Outlet Type, Outlet Size, Outlet Location Type, Outlet Establishment Year, Sales, Rating

## 🧹 Data Cleaning
- Standardized inconsistent Fat Content labels (`LF`, `low fat` → **Low Fat**; `reg` → **Regular**)
- Handled 1,463 missing values in Item Weight
- Checked data types and formatted the columns for analysis

## 📐 DAX Measures
```DAX
Total Sales   = SUM(BlinkIT_Grocery_Data[Sales])
Avg Sales     = AVERAGE(BlinkIT_Grocery_Data[Sales])
No of Items   = COUNT(BlinkIT_Grocery_Data[Item Identifier])
Avg Rating    = AVERAGE(BlinkIT_Grocery_Data[Rating])
```

## 📊 Dashboard Features
- **KPI Cards:** Total Sales, Average Sales, No. of Items, Average Rating
- **Metric switch buttons** (field parameters): toggle every visual between Total Sales, Avg Sales, No. of Items and Avg Rating
- **Filter panel:** Outlet Location Type, Outlet Size, Item Type
- **Visuals:**
  - Fat Content donut chart
  - Sales by Item Type (bar chart)
  - Fat Content by Outlet Tier (clustered bar)
  - Outlet Size donut chart
  - Outlet Location funnel
  - Outlet Establishment trend (area chart)
  - Outlet Type matrix with conditional formatting

## 📈 KPIs
| Metric | Value |
|---|---|
| Total Sales | $1.20M |
| Average Sales | $141 |
| No. of Items | 8,523 |
| Average Rating | 3.9 |

## 🔍 Key Insights
1. **Top categories:** Fruits & Vegetables ($178K) and Snack Foods ($175K) together make up ~30% of total sales. Seafood, Breakfast and Starchy Foods sell the least.
2. **Fat content:** Low Fat products bring in ~65% of sales ($776K vs $425K for Regular) and lead in every city tier.
3. **Location:** Tier 3 cities bring in the most sales ($472K, ~39%), followed by Tier 2 ($393K) and Tier 1 ($336K).
4. **Outlet size:** Medium outlets lead with $508K (~42%). High-sized outlets bring in the least ($249K).
5. **Outlet type:** Supermarket Type 1 dominates with $788K (~66% of sales).
6. **Establishment year:** Outlets set up in 2018 have the highest sales ($205K).
7. **Ratings:** The average rating stays steady at ~3.9 across all outlet types.

## 💡 Business Recommendations
- Keep stock deep in Fruits & Vegetables and Snack Foods, the core revenue drivers.
- Grow the Low Fat product range, since that's where customer demand is.
- Put expansion and marketing money into Tier 3 and Tier 2 cities.
- Promote low-performing categories (Seafood, Breakfast) through bundles and discounts.
- Use the Supermarket Type 1 model as the blueprint for new outlets.

## 🛠️ Tools Used
- **Microsoft Excel:** data source and initial review
- **Power BI Desktop:** Power Query, data modeling, DAX, field parameters, visualization

## 📁 Repository Structure
```
├── BlinkIT_Grocery_Data.xlsx   # Raw dataset
├── Blinkit_Dashboard.pbix      # Power BI dashboard file
├── dashboard.png               # Dashboard screenshot
└── README.md
```
⭐ If you found this project useful, please consider giving it a star!
