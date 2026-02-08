
# Car Sales Dashboard - Power BI Project README

> **Dynamic \& interactive Power BI dashboard** for car dealership sales performance tracking with YTD/MTD KPIs, trends, and regional analysis[^11][^12]

## 📋 Table of Contents

- [Features](#features)
- [Demo](#demo)
- [Quick Setup](#quick-setup)
- [Screenshots](#screenshots)
- [Tech Stack](#tech-stack)
- [File Structure](#file-structure)
- [Contributing](#contributing)
- [License](#license)


## ✨ Features

### **Key Performance Indicators (12 KPI Cards)**

```
┌─────────────────────────────┐
│ Sales Overview     │ Avg Price │ Cars Sold │
├────────────────────┼───────────┼───────────┤
│ YTD Sales: $2.4M   │ YTD Avg:  │ YTD Units │
│ MTD Sales: $198K   │ MTD Avg:  │ MTD Units │
│ YoY Growth: +26%   │ YoY: +6.8%│ YoY: +18% │
│ YTD-PTYD: +$500K   │ Diff: +$2K│ Diff: +9  │
└────────────────────┴───────────┴───────────┘
```


### **Interactive Visualizations (6 Charts)**

| \# | Visualization | Type | Purpose |
| :-- | :-- | :-- | :-- |
| 1 | YTD Sales Weekly Trend | Line Chart | Track weekly sales patterns |
| 2 | Sales by Body Style | Pie Chart | Distribution analysis |
| 3 | Sales by Color | Pie Chart | Color preference insights |
| 4 | Cars Sold by Region | Map Chart | Geographic performance |
| 5 | Company Sales Grid | Matrix Table | Company-wise comparison |
| 6 | Sales Details Grid | Data Table | Transaction-level details |

## 🎬 Demo

**Live Dashboard Layout** (1664×936 single-page design):

```
┌─────────────────────────────┐
│ 🎛️  Slicers: Date | Style | Color | Region │
├─────────────────────────────┤
│ 12 KPI Cards (4×3 Grid)     │
├─────────────┬──────┬────────┤
│ Body Style  │Color │ Region │
│   Pie (1)   │Pie(2)│  Map(3)│
├─────────────┬──────┼────────┤
│ Company     │      │Details │
│  Grid (4)   │Matrix│ Grid(6)│
└─────────────┴──────┴────────┘
```


## 🚀 Quick Setup

```bash
# 1. Clone/Download repository
git clone <your-repo-url>
cd CarSalesDashboard

# 2. Open in Power BI Desktop
# Double-click: CarSalesDashboard.pbix

# 3. Replace with your data
# Update Excel/CSV: Date, Model, BodyStyle, Color, Amount, Region, Company

# 4. Refresh & Publish
# Home → Refresh → Publish → [Your Workspace]
```


## 📸 Screenshots

| **KPI Overview** | **Charts Section** |
| :-- | :-- |
|  |  |

## 🛠️ Tech Stack

```
🔹 Power BI Desktop (.pbix / .pbit)
🔹 DAX (Time Intelligence: TOTALYTD, DATESMTD, SAMEPERIODLASTYEAR)
🔹 Native Visuals (Cards, Line, Pie×2, Map, Matrix×2)
🔹 Data Model (Sales + Calendar tables)
🔹 Canvas (1664×936px, 8pt grid)
```


## 💻 Core DAX Measures

```dax
-- Sales Overview
YTD Total Sales = TOTALYTD(SUM(Sales[Amount]), Calendar[Date])
MTD Total Sales = CALCULATE([YTD Total Sales], DATESMTD(Calendar[Date]))
PTYD Sales = CALCULATE([YTD Total Sales], SAMEPERIODLASTYEAR(Calendar[Date]))
YoY Growth % = DIVIDE([YTD Total Sales]-[PTYD Sales], [PTYD Sales], 0)

-- Average Price
YTD Avg Price = DIVIDE([YTD Total Sales], [YTD Cars Sold], 0)

-- Cars Sold
YTD Cars Sold = CALCULATE(COUNTROWS(Sales), TOTALYTD(Calendar[Date], Calendar[Date]))
```


## 📁 File Structure

```
CarSalesDashboard/
├── CarSalesDashboard.pbix          # Main Power BI file
├── CarSalesDashboard.pbit          # Reusable template
├── SampleData/
│   └── CarSalesData.xlsx           # Sample dataset
├── docs/
│   ├── ProjectReport.md           # Detailed documentation
│   └── SubmissionDocument.md      # Project submission
├── README.md                      # This file
└── LICENSE                        # MIT License
```


## 🎨 Design Principles Applied[^13][^11]

- **Layout**: Z-pattern reading flow (KPIs top-left)
- **Colors**: 3-5 brand colors (blue/gray palette)
- **Typography**: Hierarchical fonts (48pt KPIs → 12pt labels)
- **Grid**: 8pt alignment system
- **Mobile**: Responsive, single-page, no scrolling


## 🎛️ Interactivity

- **4 Slicers**: Date Range, Body Style, Color, Region
- **Cross-filtering**: All visuals sync automatically
- **Drill-through**: Details table → transaction level
- **Tooltips**: Enhanced with YoY context


## 🚀 Deployment Steps

1. **Local**: Open `.pbix` → Refresh data → Test slicers
2. **Publish**: `Home → Publish` → Power BI Service workspace
3. **Gateway**: Configure for live data refresh (if needed)
4. **Share**: Workspace link or embed in PowerPoint/Teams
5. **Template**: Export `.pbit` for team reuse[^14]

## 📊 Sample Data Schema

```excel
Date        | Model      | BodyStyle | Color  | Amount | Region | Company
------------|------------|-----------|--------|--------|--------|--------
2026-01-15  | Toyota Camry| Sedan    | Blue   | 28500  | Perth  | ABC Corp
2026-01-22  | Ford F150  | Truck     | Red    | 45800  | Sydney | XYZ Ltd
```


## 🤝 Contributing

1. Fork the repository
2. Import your sales dataset
3. Customize theme/measures/slicers
4. Test on mobile view
5. Submit Pull Request


***

<div align="center">
<img src="https://via.placeholder.com/800x1/0078D4/FFFFFF" height="1">
<br>
🚗💰 <strong>Transform raw sales data → actionable insights → business growth</strong>
<br><br>
[
</div>

***

**⭐ Found this helpful? Star the repo to support Power BI community projects!**[^1][^4]
<span style="display:none">[^10][^2][^3][^5][^6][^7][^8][^9]</span>

<div align="center">⁂</div>

