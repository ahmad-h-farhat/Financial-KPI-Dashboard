# 💼 Financial KPI Dashboard – SQL & Tableau 

## TL;DR
End-to-end ETL + KPI analytics workflow using **DuckDB (SQL)** with **Excel** and **Tableau** dashboard outputs (screenshots + files included).

## Artifacts (open these first)
- Excel dashboard file: `docs/etl_finance_dashboard.xlsx`
- Excel dashboard preview (PNG): `docs/dashboard_preview.png`
- Tableau dashboard preview (PNG): `docs/Tableau_Dashboard_Preview.png`
- Tableau workbook: `docs/Book1.twb`

## How to view in 60 seconds
1. Open the PNG previews in `/docs`.
2. Open `docs/etl_finance_dashboard.xlsx` (Excel dashboard).
3. Open `docs/Book1.twb` in Tableau (Tableau dashboard version).

## Quick run (optional)
1. Install DuckDB.
2. Run SQL scripts in `/etl` (load → clean → SCD).
3. Run KPI queries in `/kpi_analytics` and validate results against the dashboard outputs in `/docs`.

This project simulates a real-world ETL pipeline and KPI analytics workflow for a financial firm managing global client transactions. It uses SQL (DuckDB) for ETL + KPI calculation and produces dashboard-ready outputs in Excel and Tableau.

---

## 🧠 Business Context
A financial company handles high-volume transactions from international clients across multiple currencies. Management needs reliable KPIs to track revenue, client activity, and portfolio distribution — but raw data is messy, inconsistent, and non-standardized.

This project addresses that by building a clean ETL pipeline that transforms raw transaction data into analysis-ready tables and KPI outputs.

---

## 🚀 Solution Overview

### ETL Pipeline Flow
1. Load raw data from CSV  
2. Clean & standardize (currency conversion, date formatting, duplicate handling)  
3. Apply Slowly Changing Dimensions (SCD) to track client profile changes  
4. Generate KPIs using analytical tables  
5. Visualize results in Excel + Tableau  

---

## 🛠️ Tech Stack
- DuckDB (SQL)
- Excel (dashboard visualization)
- Tableau (dashboard visualization)
- GitHub (version control)

---

## 📁 Folder Structure
```text
Financial-KPI-Dashboard/
├── data/                      # Raw source data
│   └── transactions.csv
│
├── etl/                       # ETL SQL scripts
│   ├── load_transactions.sql
│   ├── clean_transactions.sql
│   └── scd_clients.sql
│
├── kpi_analytics/             # KPI calculation SQL queries
│   ├── revenue_by_client.sql
│   ├── daily_trading_volume.sql
│   ├── arpu.sql
│   ├── top_clients.sql
│   ├── top_clients_by_revenue.sql
│   └── portfolio_breakdown.sql
│
├── docs/                      # Deliverables
│   ├── etl_finance_dashboard.xlsx
│   ├── dashboard_preview.png
│   ├── Tableau_Dashboard_Preview.png
│   └── Book1.twb
│
└── README.md

```
---

## 📊 KPI Overview

| SQL Query                      | Description                                    |
|--------------------------------|------------------------------------------------|
| `revenue_by_client.sql`        | Total revenue per client (USD)                |
| `daily_trading_volume.sql`     | Total transaction volume per day (USD)        |
| `arpu.sql`                     | Average Revenue Per User (ARPU)               |
| `top_clients.sql`              | Top 5 clients by total revenue                |
| `top_clients_by_revenue.sql`   | Top 10 clients ranked by revenue              |
| `portfolio_breakdown.sql`      | Portfolio breakdown by asset type (USD & %)  |

---

## 📈 Dashboard Preview

Interactive Excel dashboard visualizing all KPIs and trends.

![Dashboard Preview](docs/dashboard_preview.png)

📥 [Download the full Excel Dashboard here](docs/etl_finance_dashboard.xlsx)

---
## 📊 Tableau Dashboard Overview

![Financial KPI Overview](docs/Tableau_Dashboard_Preview.png)

---

