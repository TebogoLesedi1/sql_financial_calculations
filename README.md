# SQL Financial Calculations

A comprehensive SQL Server (T-SQL) repository for financial engineering calculations and analysis. This project demonstrates advanced financial modeling using Microsoft SQL Server with GAAP-compliant data integrity standards.

## 📋 Overview

This repository contains practical financial calculation queries including:
- **Simple Interest Calculations**
- **Compound Interest Analysis** (annual, quarterly, monthly, semi-annual)
- **Hire Purchase Installments**
- **Inflation Projections**
- **Depreciation Modeling** (reducing balance method)
- **Loan Accrual Calculations**
- **Effective Annual Rate (EAR) Analysis**
- **Capital Doubling Time**

## 📁 Repository Structure

```
sql_financial_calculations/
├── README.md                          # This file
├── sql_queries/
│   └── financial_metrics.sql         # Main SQL queries and financial calculations
└── screentshoots/
    ├── git_workings.png              # Git workflow demonstration
    ├── query_overview.jpeg           # Query overview documentation
    └── query_questions.jpeg          # Assessment questions reference
```

## 🗂️ Folder Details

### `sql_queries/`
Contains the primary SQL Server script (`financial_metrics.sql`) that includes:
- Database and table creation using best practices
- Sample financial data insertion with realistic scenarios
- 10 individual financial calculation queries with detailed comments
- High-precision decimal data types (DECIMAL(19, 4)) for accurate financial computations

### `screentshoots/`
Visual documentation and reference materials:
- **git_workings.png** - Git workflow and version control demonstration
- **query_overview.jpeg** - Summary of the financial calculations covered
- **query_questions.jpeg** - Assessment questions and use cases

## 📊 Financial Formulas Implemented

| TaskID | Calculation | Formula |
|--------|-------------|---------|
| 1 | Simple Interest | I = P × r × t |
| 2 | Annual Compound Interest | A = P × (1 + r)^n |
| 3 | Hire Purchase Installment | Monthly = [P × (1 + r × t)] / 36 |
| 4 | Inflation Projection | A = P × (1 + i)^n |
| 5 | Reducing Balance Depreciation | A = P × (1 - i)^n |
| 6 | Quarterly Compounding | A = P × (1 + r/4)^(4×n) |
| 7 | Monthly Loan Accrual | I = [P × (1 + r/12)^12] - P |
| 8 | Doubling Time (Simple) | t = 1 / r |
| 9 | Effective Annual Rate (EAR) | EAR = (1 + r/m)^m - 1 |
| 10 | Semi-Annual Growth | A = P × (1 + r/2)^(2×n) |

## 🚀 Getting Started

### Prerequisites
- Microsoft SQL Server (2016 or later)
- SQL Server Management Studio (SSMS) or any T-SQL compatible client
- Basic understanding of SQL and financial calculations

### Usage

1. **Open the SQL Script:**
   - Navigate to `sql_queries/financial_metrics.sql`
   - Open in SQL Server Management Studio

2. **Execute the Script:**
   - The script will automatically create the `FinancialEngineeringDB` database if it doesn't exist
   - Creates the `FinancialTasks` table with sample data
   - Executes all 10 financial calculation queries

3. **Review Results:**
   - Each query returns calculated results with clear aliases
   - All financial values are rounded to 2 decimal places for currency precision

### Example Query

```sql
-- Simple Interest Calculation
SELECT ROUND(principal * AnnualRate * TermYears, 2) AS Simple_Interest
FROM dbo.FinancialTasks
WHERE TaskID = 1;
```

## 🔐 Data Integrity

- **Standard:** GAAP (Generally Accepted Accounting Principles)
- **Precision:** DECIMAL(19, 4) for accurate financial calculations
- **Rounding:** All results rounded to 2 decimal places for currency representation
- **Database:** Microsoft SQL Server with strict data type enforcement

## 📈 Sample Data

The repository includes 10 sample financial scenarios with varying:
- Principal amounts (₹1,550 to ₹2,500,000)
- Annual rates (5.5% to 18%)
- Terms (0 to 12 years)
- Compounding frequencies (annual, quarterly, monthly, semi-annual)

## 💡 Use Cases

- **Financial Analysis:** Quick calculation of interest earned or owed
- **Academic Projects:** Learning financial mathematics with practical SQL
- **Business Intelligence:** Building financial dashboards and reports
- **Loan & Investment Analysis:** Comparing different financial products
- **Risk Assessment:** Analyzing various financial scenarios

## 📝 Notes

- All queries include detailed comments explaining the financial logic
- Results are rounded to 2 decimal places suitable for currency calculations
- The script uses parameterized queries for flexibility
- Data is persisted in the `FinancialTasks` table for further analysis

## 🔄 Integration

This repository can be integrated with:
- Power BI for financial dashboards
- Excel via SQL connectors
- Python/R for advanced statistical analysis
- Enterprise financial systems

## 📞 Support

For questions or issues related to the financial calculations or SQL queries, please refer to:
- The inline comments in `financial_metrics.sql`
- The visual guides in the `screentshoots/` folder
- Standard SQL Server documentation

---

**Language:** T-SQL (Transact-SQL)  
**Database:** Microsoft SQL Server  
**Last Updated:** May 2026
