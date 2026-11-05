<div align="center">

# -- ! HDFC Bank Analytics — Power BI Dashboard ! --
### *3-Page Interactive Dashboard: Deposits vs Targets, Loan Portfolio & Branch Performance*

[![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![Dataset](https://img.shields.io/badge/Dataset-7%20CSV%20Files-4472C4?style=for-the-badge)](#-overview)
[![Pages](https://img.shields.io/badge/Report%20Pages-3-E31837?style=for-the-badge)](#-dashboard-pages)
[![Dashboard](https://img.shields.io/badge/Dashboard-Interactive-008C95?style=for-the-badge)](#-dashboard-pages)

<br/>

> *"Turn raw banking data into clear, interactive insights on deposits, loans and branch performance."*

</div>

---

## 📋 Table of Contents

- [📌 Overview](#-overview)
- [🎯 Problem Statement](#-problem-statement)
- [✨ Key Features](#-key-features)
- [🏗️ Project Structure](#️-project-structure)
- [🔄 Project Workflow](#-project-workflow)
- [🧹 Part A — Dataset Import](#-part-a--dataset-import)
- [🧽 Part B — Data Cleaning & Modeling](#-part-b--data-cleaning--modeling)
- [📊 Part C — KPI Analysis](#-part-c--kpi-analysis)
- [📈 Dashboard Pages](#-dashboard-pages)
- [🛠️ Tech Stack](#️-tech-stack)
- [📈 Results & Insights](#-results--insights)
- [🏆 Advantages](#-advantages)
- [📄 License](#-license)
- [👤 Author](#-author)
- [🙏 Acknowledgements](#-acknowledgements)

---

## 📌 Overview

The **HDFC Bank Analytics — Power BI Dashboard** is a 3-page Power BI report built from **7 CSV files** covering bank branches, accounts, products, dates, transactions, loan repayments and deposit targets.

The report takes the data through a complete analysis workflow:

- Import the CSV files into Power BI
- Clean, rename and model the data into a star schema
- Build DAX measures for deposits, targets, loans, EMI and transactions
- Create three linked report pages with KPI cards, charts, maps and matrices
- Add slicers, drill-down hierarchies, page navigation and a **Clear Filters** button
- Add auto-generated **Key Insights** text on every page

### 📁 Dataset Information

| Item | Details |
|------|---------|
| Source Files | 7 CSV files |
| Fact Tables | `FactTransactions`, `FactLoanRepayments`, `BranchDepositTargets` |
| Dimension Tables | `DimAccount`, `DimBranch`, `DimDate`, `DimProduct` |
| Helper Tables | `CityBands` (Deposit Band / Loan Band), `Mesure Table` (DAX measures) |
| Data as on | **30 Apr 2025** |
| Branch Network | 500 branches across 5 regions (North, South, East, West, Central) |

---

## 🎯 Problem Statement

> **Objective:** Build an interactive Power BI dashboard that shows how deposits perform against targets, how the loan book is spread across products and regions, and which branches perform best.

| 📂 Project Area | 📄 Type | 🔍 Description |
|----------------|---------|----------------|
| Raw Data | Source Data | 7 CSV files imported into Power BI |
| Data Model | Data Preparation | Star schema with fact and dimension tables, financial-year date fields |
| KPI Cards | Measures | Deposits, Target, Achievement %, Variance, Loan Book, EMI, Transactions |
| Charts | Visualization | Column, line, bar, donut, treemap, map and matrix visuals |
| Slicers | Interactivity | Financial Year, Quarter, Region, Zone, City, Branch, Product filters |
| Key Insights | Storytelling | Dynamic text measures that update with the filters |

---

## ✨ Key Features

| Feature | Description |
|--------|-------------|
| 📥 **CSV Import** | 7 CSV files loaded directly into Power BI |
| 🧹 **Data Preparation** | Columns renamed, data types fixed, financial year / quarter / month fields created |
| 📌 **KPI Cards** | Total Deposits, Deposit Target, Achievement %, Variance, Loan Book, Active Loans, EMI, Branches, Transactions |
| 🎯 **Deposits vs Target** | Monthly target vs actual deposits with product mix |
| 💰 **Loan Portfolio** | Loan book by product, region, geography and EMI trend |
| 🏦 **Branch Performance** | Branch scorecard with rank, best performing branch and transaction mix |
| 🗺️ **Map Visuals** | Bubble maps coloured by Deposit Band / Loan Band (Bottom 25%, Lower-mid 25%, Upper-mid 25%, Top 25%) |
| 🔽 **Drill-down** | Region → Zone → City → Branch and Year → Quarter → Month → Day |
| 🎛️ **Interactive Slicers** | Every slicer updates all visuals on the page |
| 🧭 **Page Navigation** | Left-side menu to jump between the three pages |
| 🧹 **Clear Filters Button** | One click to reset all slicers |
| 💡 **Key Insights** | Auto-updating insight text built with DAX |

---

## 🏗️ Project Structure

```text
📦 HDFC-PowerBI-Dashboard/
│
├── 📄 HDFC_Dashboard.pbix         ← Main Power BI report
├── 📄 README.md                   ← Project documentation
│
├── 📁 dataset/
│   ├── 📄 FactTransactions.csv
│   ├── 📄 FactLoanRepayments.csv
│   ├── 📄 BranchDepositTargets.csv
│   ├── 📄 DimAccount.csv
│   ├── 📄 DimBranch.csv
│   ├── 📄 DimDate.csv
│   └── 📄 DimProduct.csv
│
└── 📁 assets/
    ├── 🖼️ 01_deposits_vs_targets.png
    ├── 🖼️ 02_loan_portfolio.png
    └── 🖼️ 03_branch_performance.png
```

### 📚 Report Map

| Page | Purpose |
|------|---------|
| **1. Deposits vs Targets** | Compare actual deposits with targets by month, product, city and branch |
| **2. Loan Portfolio** | Loan book, active loans, EMI collection and exposure by product, region and geography |
| **3. Branch Performance** | Branch network, transactions, region performance and branch scorecard |

---

## 🔄 Project Workflow

```text
Project Start
      │
      ▼
┌────────────────────────────────────┐
│  Step 1 — Import Datasets          │
│  7 CSV files → Power BI            │
└───────────────┬────────────────────┘
                │
                ▼
┌────────────────────────────────────┐
│  Step 2 — Clean & Model Data       │
│  Rename, data types, relationships │
└───────────────┬────────────────────┘
                │
                ▼
┌────────────────────────────────────┐
│  Step 3 — Create DAX Measures      │
│  Deposits / Loans / EMI / Rank     │
└───────────────┬────────────────────┘
                │
                ▼
┌────────────────────────────────────┐
│  Step 4 — Build the 3 Pages        │
│  KPI cards, charts, maps, matrix   │
└───────────────┬────────────────────┘
                │
                ▼
┌────────────────────────────────────┐
│  Step 5 — Slicers, Navigation      │
│  Drill-down + Clear Filters        │
└───────────────┬────────────────────┘
                │
                ▼
┌────────────────────────────────────┐
│  Step 6 — Key Insights & Publish   │
│  Final interactive dashboard       │
└────────────────────────────────────┘
```

---

## 🧹 Part A — Dataset Import

### 📝 1. Source Datasets

| File | Type | Content |
|------|------|---------|
| `FactTransactions.csv` | Fact | Transactions by type (EMI, ATM, RTGS, NEFT, etc.) |
| `FactLoanRepayments.csv` | Fact | Loan repayments and EMI collections |
| `BranchDepositTargets.csv` | Fact | Deposit targets for each branch |
| `DimAccount.csv` | Dimension | Account details |
| `DimBranch.csv` | Dimension | Branch, City, Zone, Region |
| `DimDate.csv` | Dimension | Calendar and financial-year fields |
| `DimProduct.csv` | Dimension | Deposit and loan products |

### 📌 2. How to Load

1. Open Power BI Desktop
2. **Home → Get Data → Text/CSV**
3. Select each file from the `dataset/` folder (or use **Folder** to load all)
4. Click **Transform Data** to check types, then **Close & Apply**

---

## 🧽 Part B — Data Cleaning & Modeling

### 🔍 3. Preparation Steps

- Checked data types for dates, whole numbers, decimals and text
- Renamed columns and tables to clear business names
- Built financial-year fields in `DimDate` (**FY Start Year, FY Quarter, MonthKey, MonthName**)
- Created **Region → Zone → City → Branch** hierarchy from `DimBranch`
- Created **CityBands** helper table to group cities into Deposit Band and Loan Band quartiles
- Created relationships between fact and dimension tables (star schema)
- Stored all DAX measures in a dedicated `Mesure Table`

### 📊 4. Key DAX Measures

| Measure | Purpose |
|--------|---------|
| **Total Deposits** | Total deposits for the current selection |
| **Deposit Target** | Target deposits from `BranchDepositTargets` |
| **Achievement %** | Total Deposits ÷ Deposit Target |
| **Variance (Cr)** | Total Deposits − Deposit Target |
| **Total Loan Book** | Total outstanding loan amount |
| **Active Loans** | Count of active loans |
| **EMI Collection** | Total EMI collected |
| **Loan Book Share %** | Region share of total loan book |
| **Total Transactions** | Count of transactions |
| **Branch Rank** | Rank of branches by performance |
| **Best Performing Branch** | Top branch for the selection |
| **Insight Measures** | Dynamic text for Key Insights (growth, top region, top product, top transaction type) |

---

## 📊 Part C — KPI Analysis

### 💳 Page 1 — Deposits vs Targets

| KPI | Value shown |
|-----|-------------|
| **Total Deposits** | 1.78K Cr |
| **Deposit Target** | 49.32K Cr |
| **Achievement %** | 3.6% |
| **Variance (Cr)** | -47.54K |

### 💰 Page 2 — Loan Portfolio

| KPI | Value shown |
|-----|-------------|
| **Total Loan Book** | ₹ 37,567 Cr |
| **Active Loans** | 77,775 |
| **EMI Collection** | ₹ 383 Cr |
| **Avg Loan Size** | ₹ 4,830,188 |

### 🏦 Page 3 — Branch Performance

| KPI | Value shown |
|-----|-------------|
| **Total Branches** | 500 |
| **Total Transactions** | 500,000 (shown as 500000.00 Mn) |
| **Avg Transaction Value** | ₹ 250,174 |
| **Best Performing Branch** | HDFC Branch 429 |

> Values are taken from the dashboard screenshots with all filters set to **All**.

---

## 📈 Dashboard Pages

### 🎛️ Common Filters

- **Financial Year, Quarter, Region, Zone, City, Branch** (all pages)
- **Month, Product Type** (Deposits vs Targets)
- **Loan Product** (Loan Portfolio)
- **Clear Filters** button on every page

### 1️⃣ Deposits vs Targets

| Visual | What it shows |
|-------|---------------|
| **Deposit Target and Total Deposits by Month** | Monthly target against actual deposits |
| **Deposits Trend** | Year → Quarter → Month drill-down trend |
| **Deposits by Product Type** | Donut of Personal, Current, Fixed Deposit, Vehicle and Savings |
| **Total Deposits by City and Deposit Band** | Map with Deposit Band colours |
| **Branch Table** | Region, Zone, City, Branch, Target, Deposits, Achievement % and Variance |
| **Key Insights** | Target vs actual, achievement %, variance and trend |

![Deposits vs Targets Dashboard](assets/01_deposits_vs_targets.png)

### 2️⃣ Loan Portfolio

| Visual | What it shows |
|-------|---------------|
| **Loan Portfolio by Product** | Treemap of Business, Education, Personal, Vehicle and Home Loan |
| **Outstanding Loan Amount by Product** | Bar chart of outstanding amount per product |
| **EMI Collection Trend** | Year → Quarter → Month drill-down line chart |
| **Loan Exposure by Geography** | Map with Loan Band colours |
| **Loan Book by Region** | Donut of North, South, Central, West and East |
| **Loan Portfolio Matrix** | Region → Zone → Branch with Loan Book, EMI, Active Loans and Share % |
| **Key Insights** | Loan book growth, top product, top region and EMI growth |

![Loan Portfolio Dashboard](assets/02_loan_portfolio.png)

### 3️⃣ Branch Performance

| Visual | What it shows |
|-------|---------------|
| **Branch Network Performance** | Map of total deposits by branch location |
| **Deposits by Branch Hierarchy** | Region → Zone → City → Branch drill-down bar chart |
| **Transactions Trend** | Year → Quarter → Month → Day drill-down |
| **Transaction Type Distribution** | Donut of EMI, ATM, RTGS, NEFT and more |
| **Region Performance** | Deposits vs Loans by region |
| **Branch Performance Scorecard** | Deposits, Loans, Transactions, Target Achievement % and Rank |
| **Key Insights** | Deposit growth, top transaction type, top branch and top region |

![Branch Performance Dashboard](assets/03_branch_performance.png)

---

## 🛠️ Tech Stack

| Tool / Feature | Purpose |
|----------------|---------|
| 📊 **Power BI Desktop** | Report and dashboard creation |
| 📥 **CSV Datasets** | Source data |
| 🧹 **Power Query** | Data cleaning and type conversion |
| 🧮 **DAX** | KPI, ranking and insight measures |
| 🔗 **Data Modeling** | Star schema relationships |
| 📈 **Charts** | Column, line, bar, donut, treemap |
| 🗺️ **Map Visuals** | Geographic view of deposits and loans |
| 🎛️ **Slicers & Buttons** | Filters, page navigation and Clear Filters |
| 🎨 **Formatting & Icons** | HDFC-style blue and red theme |

---

## 📈 Results & Insights

- ✅ **7 CSV files** modeled into a 3-page Power BI report
- 💰 **Loan book of ₹37,567 Cr** across **77,775 active loans**, with North the largest region at ₹8,754 Cr (23.3%)
- 🏢 **Business Loan** leads with about 20.1% of the loan book
- 📊 **Total Deposits grew 49.9%** and **Total Loan Book grew 50.2%** vs the previous year
- 💳 **EMI** is the top transaction type at about 14.4% of transactions
- 🏆 **HDFC Branch 429** is the best performing branch
- 🌍 **North** leads deposits at about ₹415 Cr
- 🎯 Deposits are well below the deposit target in the current data (3.6% achievement)
- 🎛️ **Slicers and drill-downs** make it easy to analyze any region, zone, city or branch

---

## 🏆 Advantages

| Advantage | Detail |
|-----------|--------|
| 🎓 **Beginner Friendly** | Shows a complete Power BI workflow from CSV to dashboard |
| 🎛️ **Interactive** | Slicers, drill-downs and cross-filtering on every page |
| 📊 **Visual** | KPI cards, maps and charts make insights quick to read |
| 🔍 **Detailed** | Branch-level tables and matrices for deeper investigation |
| 💡 **Dynamic Insights** | Key Insights text updates automatically with filters |
| 📚 **Portfolio Ready** | Clean structure with datasets, report and screenshots |

---

## 📄 License

This project is provided for **educational and portfolio purposes**.

HDFC Bank name and logo belong to their respective owner and are used here only for a learning project.

---

## 👤 Author

<div align="center">

### HDFC Bank Analytics — Power BI Dashboard

> *"From raw rows to meaningful insights — one measure, one visual and one dashboard at a time."*

**👩‍💻 Author:** Yashvi Jasani  
**🎓 Project Type:** Power BI Data Analysis & Dashboard  
**📊 Focus:** Deposits, Loans & Branch Performance Analysis  
**🛠️ Skills:** Power BI · Power Query · DAX · Data Modeling · KPI Measures · Slicers · Drill-down · Dashboard Design

</div>

---
Video Link Here (https://drive.google.com/file/d/1ZHhnoCOs1zNUeM91mspdWoLBWF4rTLEf/view?usp=sharing)

## 🙏 Acknowledgements

This project was developed using HDFC-style banking datasets and Power BI Desktop.

Key Power BI concepts demonstrated in the project include:

- Data import, cleaning and modeling
- DAX measures and dynamic Key Insights
- KPI cards
- Drill-down charts, treemap, donut and map visuals
- Matrix and table visuals
- Slicers, page navigation and Clear Filters button
- Dashboard layout and formatting

---

<div align="center">

---

*Made with ❤️ and 📊 — Last updated: 2 November, 2026*

</div>
