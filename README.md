# Data-Analysis-Projects


> **Three production-ready Power BI dashboards** showcasing advanced DAX, data modeling, and interactive visualization for business intelligence across **Car Sales**, **Digital Marketing**, and **Credit Analysis**.

## 📋 Table of Contents

- [Project 1: Car Sales Dashboard](#project-1-car-sales-dashboard)
- [Project 2: Digital Marketing Campaigns](#project-2-digital-marketing-campaigns)
- [Project 3: Credit Analysis Dashboard](#project-3-credit-analysis)
- [Tech Stack](#tech-stack)
- [Quick Start](#quick-start)
- [File Structure](#file-structure)
- [License](#license)

***

## Project 1: Car Sales Dashboard 🚗💰

**Dynamic sales performance tracking** for car dealerships with YTD/MTD KPIs and regional analysis.

### ✨ Features

| KPI Category | Metrics |
| :-- | :-- |
| **Sales Overview** | YTD/MTD Sales, YoY Growth, YTD vs PTYD |
| **Average Price** | YTD/MTD Avg Price, YoY Growth |
| **Cars Sold** | YTD/MTD Units, YoY Growth |

### 📊 Visualizations (6 Charts)

1. YTD Sales Weekly Trend (Line)
2. Sales by Body Style (Pie)
3. Sales by Color (Pie)
4. Cars Sold by Region (Map)
5. Company Sales Grid (Matrix)
6. Sales Details Table

**Files**: `CarSalesDashboard.pbix` | `CarSalesData.xlsx`

***

## Project 2: Digital Marketing Campaigns 📈🎯

**ROI-focused marketing analytics** tracking campaign performance across channels, creatives, and audience segments.

### ✨ Features

| KPI Category | Metrics |
| :-- | :-- |
| **Campaign Performance** | Total Spend, Revenue, ROAS, CPA |
| **Channel Breakdown** | CTR, CPC, Conversion Rate by Platform |
| **Creative Analysis** | Best performing ads by CTR/Conversion |
| **Audience Insights** | Demographics, Device, Geo performance |

### 📊 Visualizations (8 Charts)

1. Campaign ROAS Trend (Line)
2. Channel Performance (Column + Line)
3. Funnel Conversion (Waterfall)
4. Geo Heatmap (Map)
5. Top Creatives (Table)
6. Audience Demographics (Donut)
7. Device Breakdown (Stacked Column)
8. Cost vs Revenue (Scatter)

**Files**: `MarketingDashboard.pbix` | `MarketingCampaigns.xlsx`

***

## Project 3: Credit Analysis 🏦📋

**Risk assessment and portfolio monitoring** for credit risk analysts with PD, LGD, and EAD modeling.

### ✨ Features

| KPI Category | Metrics |
| :-- | :-- |
| **Portfolio Health** | Total Exposure, NPL Ratio, Coverage Ratio |
| **Risk Metrics** | PD, LGD, EAD, Expected Loss |
| **Segment Analysis** | Industry, Region, Vintage performance |
| **Early Warning** | Days Past Due, Watchlist trends |

### 📊 Visualizations (7 Charts)

1. Portfolio Health KPIs (Cards)
2. NPL Trend (Line)
3. Exposure by Industry (Treemap)
4. Regional Risk Heatmap (Map)
5. Vintage Analysis (Matrix)
6. PD/LGD Scatter Plot
7. Delinquency Waterfall

**Files**: `CreditAnalysis.pbix` | `CreditPortfolio.xlsx`

***

## 🛠️ Tech Stack

```
🔹 Power BI Desktop (.pbix / .pbit templates)
🔹 DAX Advanced (Time Intelligence, What-If Parameters)
🔹 Data Modeling (Star Schema, Many-to-Many)
🔹 Native + Custom Visuals (Maps, Sankey, Decomposition Tree)
🔹 Canvas Design (1664×936, Mobile Responsive)
🔹 Data Sources (Excel, SQL, APIs)
```


## 🚀 Quick Start

```bash
# 1. Clone the portfolio
git clone <your-repo-url>
cd powerbi-portfolio

# 2. Open any dashboard
# Double-click: CarSalesDashboard.pbix
# Replace sample data → Refresh → Publish

# 3. Deploy to Power BI Service
# Home → Publish → [Your Workspace]
# Configure scheduled refresh
```


## 📁 File Structure

```
powerbi-portfolio/
├── Project 1 - Car Sales/
│   ├── CarSalesDashboard.pbix
│   ├── CarSalesDashboard.pbit
│   └── SampleData/CarSalesData.xlsx
├── Project 2 - Marketing/
│   ├── MarketingDashboard.pbix
│   └── SampleData/MarketingCampaigns.xlsx
├── Project 3 - Credit Analysis/
│   ├── CreditAnalysis.pbix
│   └── SampleData/CreditPortfolio.xlsx
├── docs/
│   ├── Project-Reports/
│   └── Submission-Documents/
├── README.md
└── LICENSE
```


## 🎨 Design Standards (All Projects)

```
✅ Single-page, mobile-responsive layouts
✅ 8pt grid system, Z-pattern reading flow
✅ 3-5 color palettes per project
✅ Hierarchical typography (48pt KPIs → 12pt labels)
✅ Cross-filtering slicers
✅ Export-ready tables
✅ Performance optimized (DAX, relationships)
```


## 📈 Sample KPIs Displayed

| Project | Key Metric | Sample Value |
| :-- | :-- | :-- |
| **Car Sales** | YTD Revenue | \$2.4M (+26% YoY) |
| **Marketing** | Campaign ROAS | 4.2x |
| **Credit** | NPL Ratio | 2.8% |

## 🎛️ Interactivity Features

- **Slicers**: Date, Category, Region, Segment
- **Drill-through**: Summary → Detail pages
- **Cross-filtering**: Click any visual to filter others
- **Bookmarks**: Saved views/states
- **Tooltips**: Context-rich hover info


## 🚀 Deployment Guide

```mermaid
graph LR
  A[Download .pbix] --> B[Import Your Data]
  B --> C[Refresh Relationships]
  C --> D[Publish to Workspace]
  D --> E[Configure Gateway]
  E --> F[Share App/Embed]
```


## 🤝 Contributing

1. Fork repository
2. Import your dataset to any project
3. Customize themes/measures/slicers
4. Test mobile responsiveness
5. Submit Pull Request



<div align="center">
<img src="https://via.placeholder.com/1000x1/0078D4/FFFFFF" height="1">
<br>
```
<strong>🚀 From raw data to executive-ready insights across Sales, Marketing, and Risk</strong>
```
<br><br>
⭐ **Star this repo** - Perfect template for Power BI interviews & portfolios!
</div>
