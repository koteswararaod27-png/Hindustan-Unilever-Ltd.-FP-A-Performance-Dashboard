**Hindustan Unilever Ltd. – FP&A Performance Dashboard**


FP&amp;A dashbo# FP&A Performance Dashboard — Budget vs Actual Analysis (HUL Financial Data)

## 📌 Overview
An FP&A (Financial Planning & Analysis) dashboard built in **Power BI**, using real quarterly financial data (Revenue, Expenses, Operating Profit, EBIT, Other Income, Interest, EBT, Tax, Net Profit) exported from **Screener.in** for a listed FMCG company. The project simulates a typical corporate FP&A workflow: pulling actuals, building a budget/forecast, running variance analysis, and summarizing insights for management.

> Note: Company financials used here are public data (via Screener.in) used purely for portfolio/practice purposes — this is not an official or affiliated company report.

## 🎯 Objective
- Build a Budget from historical trailing-quarter averages (growth rates & margins)
- Compare Actual vs Budget across the full P&L (Revenue → Net Profit)
- Calculate variance (₹ and %) and flag Favorable/Unfavorable performance per line item
- Summarize findings into management-ready KPIs and commentary
- Visualize everything in an interactive Power BI dashboard

## 🗂️ Data & Methodology
**Source workbook** (`Hind__Unilever.xlsx`) contains:
| Sheet | Purpose |
|---|---|
| Data Sheet / P&L / Balance Sheet / Cash Flow | Raw historical financials (FY2017–FY2026, annual + quarterly) |
| Histarical | Quarterly actuals broken into margin ratios (OPM, EBIT Margin, NP Margin, etc.) |
| Budget_Assumptions | Trailing 6-quarter average growth % and margin % used as budget drivers |
| Budgets | Forecasted Revenue → Net Profit for the next 4 quarters, built from those assumptions |
| Revenue Analysis / Cost Analysis / Operating Profit Analysis / EBIT Analysis / Other Income / Interest Exp / EBT / TAX / Net Profit | Line-by-line Actual vs Budget variance analysis with FP&A commentary per quarter |
| Executive Summary | Consolidated KPI table + management insights + recommended actions |
| Rolling Forecasting / RF Summary | 4-quarter rolling forecast extending performance trends |
| Dashbord | Flat table combining all Actual/Budget/Variance columns — feeds the Power BI visuals |

**Budget logic:** Each budget driver (Revenue Growth %, Expenses % of Sales, Operating Margin, EBIT Margin, Other Income % of Sales, Interest % of Sales, Tax % of Sales) is the **average of the trailing 6 quarters**, then applied forward to project the next 4 quarters.

## 📊 Dashboard KPIs
- **Revenue Growth %**
- **EBITDA Margin %**
- **EBIT Margin %**
- **Net Profit Margin %**
- Revenue / Operating Profit / EBIT / Net Profit — Budget vs Actual (bar charts, by quarter)
- Cost Analysis and Other Income — quarterly breakdown (donut charts)

## 🔍 Key Insights
- Revenue was above budget in all 4 quarters, with the largest favorable variance (+6.84%) in Jun-26
- Expenses also exceeded budget every quarter — Jun-26 expense growth (+7.98%) outpaced revenue growth (+6.84%), signaling margin pressure
- Operating Profit and EBIT stayed above budget throughout, showing resilient core operating performance
- Other Income was highly volatile (e.g. +1,282.75% variance in Dec-25), materially distorting EBT and Net Profit in that quarter
- Interest expense came in below budget in 3 of 4 quarters, partially offsetting cost pressure
- Net Profit was above budget in only 2 of 4 quarters — once the Other Income spike is excluded, underlying profitability was mixed

## ⚠️ Known Limitation
The **Net Profit Margin** KPI card needs a formula check — it should be calculated as `Net Profit ÷ Revenue`, but the current measure may be referencing a growth-rate column instead of a true margin, producing inconsistent results against the EBIT Margin card. Recommended fix before final publishing.

## 🛠️ Tools Used
- **Excel** — data modeling, budget assumptions, variance calculations
- **Power BI** — dashboard visualization, DAX measures, slicers
- **Screener.in** — source financial data

## 👤 Author
Dharaniboina Koteswara Rao — MBA Finance | Aspiring Financial Analyst / FP&Aard for Hindustan Unilever Ltd. analyzing Actual vs Budget vs Rolling Forecast performance across Revenue, EBITDA, EBIT, and Net Profit using Excel and Power BI.
