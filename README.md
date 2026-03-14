# Bank_Loan_Report: Interactive Excel Dashboard

## Project Overview

![Bank Loan Report Banner](images/dashboard_overview.png)

This project is an end-to-end **Bank Loan Analysis Dashboard** built entirely in Microsoft Excel. It transforms raw financial loan data into a fully interactive, multi-page reporting suite — covering portfolio KPIs, good vs bad loan segmentation, and dimensional breakdowns — giving stakeholders a clear picture of lending performance without any external BI tool.

---

## Dashboard Previews

### 📋 Summary Dashboard
> Portfolio health at a glance — Good Loan vs Bad Loan breakdown, loan status table, and MTD/MOM KPI cards.

![Bank Loan Report - Summary](images/dashboard_summary.png)

---

### 🗺️ Overview Dashboard
> Dimensional analysis — Applications by month, US state, employment length, purpose, term, and home ownership.

![Bank Loan Report - Overview](images/dashboard_overview.png)

---

## Key Metrics at a Glance

| Metric | Total | MTD | MOM Change |
|---|---|---|---|
| Total Loan Applications | 38.6K | 4.3K | +6.9% |
| Total Funded Amount | $435.8M | $54.0M | +13.0% |
| Total Amount Received | $473.1M | $58.1M | +15.8% |
| Avg Interest Rate | 12.05% | 12.36% | +3.5% |
| Avg Debt-to-Income (DTI) | 13.33% | 13.67% | +2.7% |

---

## Loan Quality Segmentation

| Segment | Applications | Funded Amount | Amount Received | Share |
|---|---|---|---|---|
| ✅ Good Loans | 33.2K | $370.2M | $435.8M | **86.18%** |
| ❌ Bad Loans | 5.3K | $65.5M | $37.3M | **13.82%** |

---

## Project Steps

### 1. Data Collection & Loading
- **Source**: Raw bank loan dataset (CSV format).
- Dataset fields include: `loan_id`, `issue_date`, `loan_status`, `purpose`, `grade`, `emp_length`, `home_ownership`, `funded_amnt`, `total_payment`, `int_rate`, `dti`, `address_state`.

### 4. Pivot Table Analysis
Built structured PivotTables as the data engine powering every chart:
- Monthly application volume and MOM growth.
- Good Loan vs Bad Loan count, funded amount, and amount received.
- Applications segmented by `purpose`, `emp_length`, `grade`, `term`, and `home_ownership`.
- Loan status breakdown (Fully Paid / Charged Off / Current) across all 5 KPIs.
- State-level aggregation for the US map visual.

### 5. Dashboard Design — Summary Page
- **5 KPI Cards**: Total Applications, Funded Amount, Amount Received, Avg Interest Rate, Avg DTI — each showing Total, MTD, and MOM values.
- **Good Loan Section**: Donut chart (86.18%) + 3 metric tiles (applications, funded, received).
- **Bad Loan Section**: Donut chart (13.82%) + 3 metric tiles.
- **Loan Status Table**: Side-by-side bar comparison for Fully Paid, Charged Off, and Current across all 5 KPIs.

### 6. Dashboard Design — Overview Page
- **Line Chart**: Total Loan Applications by Month (Jan–Dec trend).
- **Filled Map**: Total Loan Applications by US State using Excel's built-in Map Chart.
- **Horizontal Bar Chart**: Applications by Employment Length.
- **Horizontal Bar Chart**: Applications by Purpose (Debt Consolidation, Credit Card, etc.).
- **Donut Chart**: Applications by Term (36 months vs 60 months).
- **Stacked Bar Chart**: Applications by Home Ownership (Rent, Mortgage, Own).

### 7. Interactivity — Slicers
- **Grade Slicer**: Filter all visuals by loan grade (A through G).
- **Purpose Slicer**: Filter by loan purpose (Car, Credit Card, Debt Consolidation, Educational, Home Improvement, etc.).
- Slicers connected to all PivotTables via **Report Connections** for synchronized cross-page filtering.

### 8. Formatting & Polish
- Dark navy theme applied using custom cell styles and chart area formatting.
- Gridlines, row/column headers hidden on all dashboard sheets for a clean look.
- Navigation buttons (Summary / Overview / Details) added using Shapes with hyperlinks.
- Consistent typography and white-on-dark color scheme throughout.

---

## Tools Used

| Tool | Purpose |
|---|---|
| Microsoft Excel | End-to-end dashboard development |
| Power Query | Data import, cleaning & transformation |
| PivotTables | Aggregation and metric calculation |
| Excel Charts | Line, Bar, Donut, Map, Stacked Bar visuals |
| Slicers | Interactive cross-page filtering |
| Conditional Formatting | KPI highlights and status indicators |

---

## Project Structure

```plaintext
|-- data/
|   |-- financial_loan.csv          # Raw dataset
|-- Bank_Loan_Report.xlsx           # Main Excel workbook
|   |-- Sheet: Raw_Data             # Cleaned source data table
|   |-- Sheet: Pivot_Tables         # All PivotTable calculations
|   |-- Sheet: Summary              # Summary Dashboard
|   |-- Sheet: Overview             # Overview Dashboard
|   |-- Sheet: Details              # Row-level drill-through table
|-- README.md
```

---

## Results and Insights

- **Loan Volume Growth**: Applications grew from 2.3K in January to 4.3K in December — an **+87% increase** over the year, with the strongest momentum in Q4.
- **Portfolio Quality**: 86.18% of loans are performing (Fully Paid or Current). Charged Off loans represent 13.82% — totalling **$65.5M in bad debt exposure**.
- **Top Loan Purpose**: Debt Consolidation leads with **18.2K applications** (~47% of total); Credit Card refinancing follows at 5.0K.
- **Employment Tenure**: Borrowers with 10+ years of employment form the largest segment (8.9K), reflecting lender preference for financial stability.
- **Loan Term Split**: 60-month loans (28.2K) significantly outnumber 36-month terms (10.3K), indicating borrowers prefer lower monthly installments.
- **Home Ownership**: Renters (18.4K) slightly edge out Mortgage holders (17.2K) in total applications.
- **Interest Rate as Risk Signal**: Charged Off loans carry a higher avg interest rate (13.9%) versus Fully Paid loans (11.6%), confirming rate as a default predictor.

---

## Future Enhancements

- Connect the workbook to a live source via **Power Query ODBC** for automated monthly refresh.
- Add a **Details drill-through page** with a searchable, filterable loan-level table.
- Introduce **VBA macros** for one-click PDF export of the dashboard.
- Migrate to Power BI for datasets exceeding Excel's row limit.

---

## Acknowledgments

- **Inspiration**: Real-world bank loan monitoring and credit risk reporting workflows.

---

## Author — Abhisek Nayak

This project is part of my portfolio, showcasing Excel data modeling, PivotTable design, and financial dashboard skills essential for Data and Business Analyst roles. Feel free to connect or collaborate.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abhisek-nayak-88054a362/)
