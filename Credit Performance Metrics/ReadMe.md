
# Credit Performance Metrics Dashboard 🏦📊

> **Production-ready Power BI dashboard** for comprehensive **loan portfolio monitoring** with Good/Bad Loan analysis, regional insights, and lending trend tracking.

<div align="center">
  <strong>Financial Risk Management | Loan Performance Analytics | Portfolio Health</strong>
</div>

## 📋 Table of Contents

- [Business Objective](#business-objective)
- [🔑 Key Performance Indicators](#key-performance-indicators)
- [📊 Interactive Visualizations](#interactive-visualizations)
- [🚀 Quick Setup](#quick-setup)
- [📈 Good vs Bad Loan Analysis](#good-vs-bad-loan-analysis)
- [📁 File Structure](#file-structure)
- [🎨 Design Standards](#design-standards)

***

## 🎯 Business Objective

**Monitor loan portfolio health and identify risk patterns** through:

- ✅ Total applications, funding, and repayment tracking
- ✅ Good vs Bad loan performance analysis
- ✅ Regional lending performance insights
- ✅ Borrower profile analysis (employment, home ownership, purpose)
- ✅ Seasonal trend identification


## 🔑 Key Performance Indicators

### Core Portfolio KPIs

| KPI | Definition | Time Intelligence |
| :-- | :-- | :-- |
| **Total Loan Applications** | All loan applications received | YTD + MTD |
| **Total Funded Amount** | Total loans disbursed | YTD + MTD |
| **Total Amount Received** | Principal + interest repayments | YTD + MTD |
| **Average Interest Rate** | Portfolio avg interest rate | Current portfolio |
| **Average DTI** | Avg Debt-to-Income ratio | Borrower health indicator |

### Good vs Bad Loan Analysis

```
GOOD LOANS: Successfully repaid on time
BAD LOANS: Defaulted / Written off
```

| Category | Good Loans | Bad Loans |
| :-- | :-- | :-- |
| **Application %** | % of total apps | % of total apps |
| **Applications** | \# Good loan apps | \# Bad loan apps |
| **Funded Amount** | \$ Good loans funded | \$ Bad loans funded |
| **Amount Received** | \$ Recovered from good | \$ Recovered from bad |

## 📊 Interactive Visualizations (7 Charts)

```
┌─────────────────────────────┐
│ 🎛️ Slicers: Date | Region | Loan Status │
├─────────────┬──────┬───────┤
│ Monthly     │State │ Loan  │
│  Trend      │Bars │ Term  │
│ (Line)      │     │Donut │
├─────────────┼──────┼──────┤
│ Emp Length │Purpose│Home   │
│   Bars     │ Bars │Owner │
│            │      │Heatmap│
└─────────────┴──────┴──────┘
```

| \# | Visualization | Type | Purpose |
| :-- | :-- | :-- | :-- |
| 1 | **Monthly Trends** | Line/Area | Seasonality \& growth patterns |
| 2 | **Regional Analysis** | Bar Chart | State-wise performance |
| 3 | **Loan Term** | Donut Chart | Distribution by term length |
| 4 | **Employee Length** | Bar Chart | Employment history impact |
| 5 | **Loan Purpose** | Bar Chart | Primary financing reasons |
| 6 | **Home Ownership** | Treemap/Heatmap | Housing status analysis |
| 7 | **KPI Cards** | Cards (12) | Good/Bad loan metrics |

**Dynamic Metrics**: Total Applications | Funded Amount | Amount Received

## 🚀 Quick Setup

```bash
# 1. Clone/Download repository
git clone <your-repo-url>
cd credit-analysis-dashboard

# 2. Open in Power BI Desktop
double-click CreditAnalysisDashboard.pbix

# 3. Connect your loan data
# Required: loans, applications, repayments tables
# Refresh relationships → Test slicers

# 4. Publish to Power BI Service
Home → Publish → [Your Workspace]
```


## 📈 Good vs Bad Loan Analysis

**DAX Measures**:

```dax
Total Applications = COUNT(Loans[ApplicationID])
Good Loan % = DIVIDE([Good Loan Applications], [Total Applications], 0)
Bad Loan Funded = CALCULATE([Total Funded Amount], Loans[LoanStatus] = "Bad")
Good Loan Received = CALCULATE([Total Amount Received], Loans[LoanStatus] = "Good")

MTD Applications = CALCULATE([Total Applications], DATESMTD('Calendar'[Date]))
```

**Color Coding**:

- ✅ **Green**: Good Loans (On-time repayment)
- ❌ **Red**: Bad Loans (Defaulted/Written-off)


## 🛠️ Data Model

```
Loans[issue_date] ←── Loans ←── Repayments
         ↓                    ↓
'Calendar'[Date]    LoanStatus (Good/Bad)
         ↓
Applications[employee_length] → slicers
```

**Required Columns**:

```
Loans: ApplicationID, issue_date, funded_amount, interest_rate, 
       dti, loan_term, loan_purpose, home_ownership, state, loan_status
Repayments: loan_id, amount_received, repayment_date
```


## 📁 File Structure

```
credit-analysis-dashboard/
├── CreditAnalysisDashboard.pbix     # Main dashboard
├── CreditAnalysisDashboard.pbit     # Template file
├── SampleData/
│   ├── loans.xlsx
│   ├── repayments.xlsx
│   └── applications.xlsx
├── docs/
│   └── BRD.md                       # Business Requirements
├── README.md                        # This file
└── LICENSE
```


## 🎨 Design Standards

```
✅ Single-page responsive layout (1664×936px)
✅ Financial color scheme (Green/Red/Blue/Gray)
✅ Z-pattern reading flow (KPIs → Trends → Breakdowns)
✅ Mobile-optimized typography
✅ Conditional formatting (Good=🟢 Bad=🔴)
✅ Export-ready tables with drill-through
```


## 📱 Slicer Controls

- **Date Range** (Syncs monthly trends + MTD KPIs)
- **Region/State** (Filters maps + regional bars)
- **Loan Status** (Good/Bad toggle)
- **Metrics Selector** (Applications/Funded/Received)


## 🎛️ Interactivity Features

- **Cross-filtering**: Click any visual → filters portfolio
- **Drill-through**: State → Individual loans
- **Bookmarks**: Good Loans | Bad Loans | Regional views
- **Dynamic titles**: "MTD Funded Amount: \$2.4M"
- **What-if parameters**: Stress test scenarios



## 📊 Sample Insights Generated

| Analysis | Key Finding | Business Action |
| :-- | :-- | :-- |
| **Top State** | California: 28% applications | ✅ Increase regional staffing |
| **Risk Pattern** | Bad Loans peak Dec-Jan | ⚠️ Tighten holiday lending |
| **Employee Length** | 10+ yrs: 82% good loans | ✅ Prioritize experienced borrowers |
| **Loan Purpose** | Debt Consolidation: highest volume | 📈 Targeted marketing campaign |

## 📈 Sample KPI Cards Display

```
┌─────────────────────────────┐
│ Total Apps: 12,847 │ Funded: $245M │
├────────────────────┼───────────────┤
│ MTD Apps: 1,234    │ MTD Funded:  │
│                    │ $23.4M        │
├────────────────────┼───────────────┤
│ Good Loans: 92%    │ Bad Loans: 8% │
└────────────────────┴───────────────┘
```


## 🤝 Contributing

1. Fork repository
2. Add your loan dataset
3. Customize risk thresholds
4. Test mobile responsiveness
5. Submit Pull Request



