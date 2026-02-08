
# Digital Marketing Campaigns Analysis Dashboard 🚀

> **Production-ready Power BI dashboard** for Facebook & Instagram ad campaigns tracking **reach, engagement, conversions, and ROI** with dynamic metric switching and geographic insights.



## 📋 Table of Contents
- [Business Objective](#business-objective)
- [🔑 Key KPIs](#key-kpis)
- [📊 Interactive Visuals](#interactive-visuals)
- [🚀 Quick Setup](#quick-setup)
- [📈 Dynamic Parameters](#dynamic-parameters)
- [📁 File Structure](#file-structure)
- [🎨 Design Standards](#design-standards)

---

## 🎯 Business Objective

**Track & optimize Meta ad performance** across Facebook & Instagram to:
- ✅ Identify top-performing platforms
- ✅ Maximize campaign ROI
- ✅ Optimize budget allocation
- ✅ Understand audience patterns

**Scope**: Facebook + Instagram paid ads only (No Messenger/Audience Network/Organic)

## 🔑 Key KPIs

| KPI | Definition | Formula | Purpose |
|----|------------|---------|---------|
| **Impressions** | Times ads displayed | `COUNT(event_type = "Impression")` | Measure reach |
| **Clicks** | User clicks on ads | `COUNT(event_type = "Click")` | Engagement intent |
| **Shares** | Ads shared by users | `COUNT(event_type = "Share")` | Viral potential |
| **Comments** | User comments | `COUNT(event_type = "Comment")` | Sentiment feedback |
| **Purchases** | Post-ad conversions | `COUNT(event_type = "Purchase")` | Revenue impact |
| **CTR** | Click Through Rate | `(Clicks ÷ Impressions) × 100` | Ad effectiveness |
| **Engagement Rate** | Total interactions/impressions | `(Engagements ÷ Impressions) × 100` | Overall appeal |
| **Conversion Rate** | Purchases from clicks | `(Purchases ÷ Clicks) × 100` | Funnel efficiency |

## 📊 Interactive Visuals (7 Charts)

```

┌─────────────────────────────┐
│ 🎛️ Parameter: Impressions │ Clicks │ Purchases │
├─────────────────────────────┤
│ Gender  │ Age Group │ Country │ Calendar │
│ Donut   │  Bar     │  Map    │  Heatmap │
├──────────┬──────────┼─────────┤
│ Weekly  │ Hourly   │ Ad Type │
│ Trend   │  Trend   │ Matrix  │
└──────────┴──────────┴─────────┘

```

| # | Visual | Type | Dimension | Purpose |
|---|--------|------|-----------|---------|
| 1 | **Target Gender** | Donut Chart | Gender | Gender performance split |
| 2 | **Age Group** | Bar Chart | Age Groups | Age responsiveness |
| 3 | **Country** | Map | Country | Geographic insights |
| 4 | **Calendar Month** | Heatmap | Month | Seasonal trends |
| 5 | **Weekly Trend** | Stacked Column | Week + Ad Type | Weekly patterns |
| 6 | **Hourly Trend** | Area Chart | Hour of Day | Daily activity |
| 7 | **Ad Type Matrix** | Matrix | Ad Type × Platform | Cross-comparison |

## 🚀 Quick Setup

```bash
# 1. Clone/Download repo
git clone <your-repo-url>
cd meta-ad-dashboard

# 2. Open Power BI Desktop
double-click MetaAdPerformance.pbix

# 3. Connect your data
# Required tables: ads, ad_events, users, campaigns
# Update connections → Refresh

# 4. Publish & Share
Home → Publish → Power BI Service
```


## 📈 Dynamic Parameters

**Single Parameter controls ALL visuals simultaneously**:

```dax
Metric Selector = {
    ("Impressions", "Impressions", 0),
    ("Clicks", "Clicks", 1),
    ("Purchases", "Purchases", 2),
    ("CTR %", "CTR %", 3),
    ("Engagement Rate %", "Engagement Rate %", 4)
}
```

**DAX Measures** (auto-switch based on parameter):

```dax
Dynamic Metric = 
VAR SelectedMetric = SELECTEDVALUE(Parameter[Metric Name])
RETURN
SWITCH(SelectedMetric,
    "Impressions", [Impressions],
    "Clicks", [Clicks],
    "Purchases", [Purchases],
    "CTR %", [CTR],
    "Engagement Rate %", [Engagement Rate],
    BLANK()
)
```


## 🛠️ Data Model

```
ads[gender] ←── ads ←── ad_events → Date Table → Week/Month
                ↓
campaigns[total_budget]    users[country]
                ↓
ad_events[event_type] → Dynamic Metric Parameter
```

**Required Columns**:

```
ads: ad_id, gender, age_group, ad_type, platform
ad_events: timestamp, event_type, ad_id
users: user_id, country
campaigns: campaign_id, total_budget
```


## 📁 File Structure

```
meta-ad-dashboard/
├── MetaAdPerformance.pbix          # Main dashboard
├── MetaAdPerformance.pbit          # Template
├── SampleData/
│   ├── ads.xlsx
│   ├── ad_events.xlsx
│   ├── users.xlsx
│   └── campaigns.xlsx
├── docs/
│   └── BRD.md                      # Business Requirements
├── README.md                       # This file
└── LICENSE
```


## 🎨 Design Standards

```
✅ Single-page responsive layout (1664×936)
✅ Dynamic parameter-driven visuals
✅ Z-pattern reading flow
✅ Branded Meta colors (blue/purple)
✅ Mobile-optimized
✅ Export-ready matrix
✅ Cross-filtering slicers
```


## 📱 Slicer Controls

- **Metric Selector** (Impressions/Clicks/Purchases/CTR/Engagement Rate)
- **Platform** (Facebook/Instagram)
- **Date Range**
- **Campaign Selection**


## 🎛️ Interactivity Features

- **Dynamic Metrics**: One slicer changes ALL 7 visuals
- **Cross-filtering**: Click any visual → filters others
- **Drill-through**: Country map → detailed events
- **Bookmarks**: Saved metric/platform views
- **Tooltips**: KPI definitions + values



## 📊 Sample Insights Generated

| Scenario | Key Finding |
| :-- | :-- |
| **Best Gender** | Females: 62% of purchases |
| **Peak Hours** | 8-10 PM (3x morning traffic) |
| **Top Country** | USA (45% impressions) |
| **Best Ad Type** | Video (2.1x CTR vs Image) |


---
