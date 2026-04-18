# 📊 Delta Industrial Supplies — Sales & Inventory Analysis

> ⚠️ **Confidentiality Notice:** All data in this repository has been replaced with **dummy / synthetic data** to protect the confidentiality of the business. The analysis structure, formulas, dashboards, and methodology are fully real — only the underlying figures have been anonymized.

---

## 🧭 What This Project Is

This is a comprehensive **sales intelligence and inventory analysis** built for an industrial hardware and equipment distributor. The goal: move away from intuition-based stocking decisions toward a **data-backed, demand-driven purchasing strategy**.

The analysis covers **21 months of sales and purchase data (Jul 2024 – Mar 2026)** and is delivered in two formats:
- A **g-sheet Excel workbook** with a full analytical pipeline
- **3 standalone HTML dashboards** that run directly in the browser — no server, no setup

---

## 📁 Repository Structure

```

├── Business_Data_Analysis_Template_V2.xlsx ← Main workbook (dummy data)
├── dashboard.html                   ← Sales Intelligence Dashboard
├── explorer_dashboard.html          ← Sales Explorer Dashboard
├── dashboard_ready.html             ← Bulk Purchase Analysis Dashboard
└── README.md                        ← You are here
```

---

## 🗂️ Excel Workbook — Sheet by Sheet

The workbook follows a clean pipeline from raw data to actionable output:

```
Sales Register + Purchase Register   (raw Tally export)
         ↓
Sales Analysis                        (KPI dashboard + 4 charts)
         ↓
Group Scorecard                       (40 groups ranked with health verdicts)
         ↓
Bulk Order Guide                      (group-wise purchasing report)
         ↓
Group Explorer                        (flat filterable item table)
```

---

### Sheet 1 — Sales Register
- ~10,000+ line items across 22 columns
- Each row = one item sold on one invoice
- Key fields: Party Name, Item Name, Item Group, Quantity, Rate, Purchase Rate, Margin, Amount, GST
- Source: Tally ERP export (static, no formulas)

### Sheet 2 — Purchase Register
- ~5,000+ line items across 23 columns
- Purchase-side counterpart to the Sales Register
- Includes supplier contact details not present in Sales Register

### Sheet 3 — Sales Analysis *(Main Dashboard)*
**KPI Row:** Revenue · Margin · Margin% · Item Count · Party Count · Voucher Count · Groups

**9 Analytical Sections:**
1. Monthly Sales Trend (21 months)
2. Top 20 Items by Revenue
3. Top 20 Items by Quantity
4. Top 10 Item Groups by Revenue
5. Top 15 Parties by Purchase Amount
6. Negative Margin Items — loss-makers flagged in red
7. Bulk Purchase Recommendations — flagged in green
8. Growing Demand Items (recent 6-month vs prior 6-month)

**4 Charts:** Monthly Trend (line) · Top Items by Revenue (bar) · Group Revenue Share (doughnut) · Monthly Margin % (column)

### Sheet 4 — Group Scorecard
Strategic ranking of all **40 product groups** with health verdicts.

**13 metrics per group:** Rank · Revenue · Margin · Margin% · Qty · Unique Items · Unique Buyers · Txn Count · Fragmentation Score · Concentration Risk% · Demand Trend% · **Health Verdict**

| Verdict | What It Means |
|---|---|
| ✅ STRONG | High revenue, healthy margin, broad buyer base |
| 🟢 HEALTHY | Solid performance with minor concerns |
| 🟡 WATCH | Margin pressure or declining demand — needs attention |
| 🔴 AVOID | Negative margin — review or exit |

### Sheet 5 — Bulk Order Guide
- Presentation-ready, group-sectioned purchasing report
- 40 group banners with group-level stats + ~480 item rows
- Per-item verdicts: **TOP PICK → MONITOR → RISKY → LOSS MAKER**
- Designed for printing or sharing with purchase/procurement teams

### Sheet 6 — Group Explorer
- Flat, filterable Excel Table with all ~1,985 items
- Sorted by Group (A→Z), then Revenue (high→low) within each group
- 10 columns: Group · Item · Revenue · Margin% · Qty · Avg Rate · Txns · Buyers · Verdict · Verdict Rank
- Verdict Rank (1–5) enables native Excel sorting by performance
- Dark navy headers, banded rows, frozen panes, AutoFilter enabled

---

## 🌐 HTML Dashboards

All three dashboards are **self-contained HTML files** — no installation, no backend, no internet connection required after download. Just open in any browser.

### 1. `dashboard.html` — Sales Intelligence Dashboard
A high-level executive view with:
- Macro KPIs (Revenue, Margin, Margin%, Items, Parties, Vouchers)
- Negative Margin items flagged with context
- Best Margin performers highlighted
- Bulk Recommendation scores via visual progress bars

### 2. `explorer_dashboard.html` — Sales Explorer
A granular drill-down tool:
- **3 tabs:** Group Explorer · Item Explorer · Comparison
- Filter items by verdict (Star / Healthy / Average / Weak / Risky)
- Interactive Chart.js graphs: monthly revenue, margin trends, top buyers, item composition
- Detailed data tables per product: revenue, margin%, avg rate, transactions, buyer count

### 3. `dashboard_ready.html` — Bulk Purchase Analysis
Optimized for purchasing decisions:
- **4 tabs:** Group Overview · Group Detail · Item Explorer · Bulk Recommendations
- Group health verdicts with concentration risk and demand trend signals
- "Top Bulk Picks Across All Groups" — actionable stocking targets
- "Loss-Making Items to Avoid" — flagged clearly to prevent bad inventory buys

---

## ⚙️ Tech Stack

| Tool | Usage |
|---|---|
| Microsoft Excel | Full 6-sheet analytical pipeline |
| HTML / CSS / JavaScript | All three interactive dashboards |
| Chart.js | Charts and graphs across dashboards |
| Tally ERP | Original data source (exported, anonymized here) |
| Shortcut AI | Used to accelerate analysis and dashboard generation |

---

## 🔒 Confidentiality & Usage

- All data in this repository is **dummy/synthetic** and does not reflect real business figures
- Item names, party names, rates, and all financial figures have been replaced or randomized
- The analytical structure, formulas, and dashboard logic are original and free to reference or adapt
- Please do not use this repository to infer anything about the actual business

---

## 🙋 About

Built as part of an extended engagement with a real industrial distribution business in India. The template is open for anyone working on similar inventory or sales analysis problems for small and medium businesses.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/kasim-dhila)

Feel free to open an issue or connect on LinkedIn if you have questions.
