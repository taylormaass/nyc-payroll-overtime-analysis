# NYC Payroll Overtime Analysis | Fiscal Year 2025

## Project Overview

This project examines overtime spending and hours across three New York City agencies—the Police Department (NYPD), Fire Department (FDNY), and Department of Sanitation (DSNY)—using fiscal year 2025 payroll records.

Using **Microsoft Excel and Power Query**, I prepared and validated payroll data, calculated agency-level metrics, and built a dashboard comparing overtime spending, pay, and hours.

## Business Questions

- Which of the three agencies has the highest total overtime spending?
- How does average overtime pay per payroll record compare across agencies?
- Which agency has the highest average overtime hours per payroll record?
- What potential data-quality exceptions appear in the payroll records?

## Tools and Skills

- **Excel:** KPI summaries, charts, dashboard design, and formatting
- **Power Query:** data preparation, data type transformations, grouping, and aggregation
- **Data validation:** consistency checks, exception categorization, and record-count reconciliation
- **Data storytelling:** agency comparisons and clear presentation of findings

## Dataset and Scope

- **Source:** [NYC Open Data — Citywide Payroll Data (Fiscal Year)](https://data.cityofnewyork.us/City-Government/Citywide-Payroll-Data-Fiscal-Year-/k397-673e)
- **Fiscal year:** 2025
- **Agencies:** NYPD, FDNY, and DSNY
- **Payroll records analyzed:** 85,901

**Important:** Payroll records do not necessarily represent unique employees. Per-record averages should not be interpreted as per-employee averages.

## Data Preparation and Validation

1. Imported FY2025 payroll data into Excel Power Query.
2. Reviewed and transformed column data types.
3. Applied an overtime consistency check to flag records requiring review.
4. Grouped records by agency to calculate payroll record counts, total overtime spending, total overtime hours, and average overtime pay.
5. Calculated average overtime hours per payroll record and built the Excel dashboard.

### Overtime Consistency Check

| Validation category | Records |
|---|---:|
| Consistent | 84,935 |
| Review: Pay Without Hours | 843 |
| Review: Negative Value | 120 |
| Review: Hours Without Pay | 3 |
| **Total** | **85,901** |

**966 records** were flagged for review. A flag indicates a potential inconsistency, not necessarily a confirmed error. The agency-level summaries cover all 85,901 records, including flagged records.

## Dashboard KPIs

| Metric | Value |
|---|---:|
| Total overtime spending | $1.86B |
| Total overtime hours | 24.54M |
| Payroll records | 85,901 |
| Highest agency average overtime hours per payroll record | 373.34 |

## Agency Comparison

| Agency | Payroll records | OT spending | OT hours | Average OT pay per record | Average OT hours per record |
|---|---:|---:|---:|---:|---:|
| NYPD | 55,424 | $1,087.6M | 14.81M | $19,624 | 267.28 |
| FDNY | 19,333 | $568.0M | 7.22M | $29,381 | 373.34 |
| DSNY | 11,144 | $203.8M | 2.51M | $18,284 | 225.33 |

*Values are rounded for presentation. Average overtime pay is calculated using the Average operation in Power Query; the metrics are per payroll record rather than per unique employee.*

## Key Findings

1. **NYPD led total overtime spending**, with approximately $1.09B, representing 58.5% of spending across the three agencies.
2. **FDNY had the highest average overtime hours**, at 373.34 hours per payroll record—approximately 39.7% higher than NYPD.
3. **FDNY had the highest average overtime pay per payroll record**, at approximately $29,381, compared with $19,624 for NYPD and $18,284 for DSNY.
4. **Total spending and per-record metrics tell different stories:** NYPD had the largest spending total and payroll record count, while FDNY led both per-record averages shown.

## Dashboard Preview

![NYC Overtime Dashboard](screenshots/nyc_overtime_dashboard.png)

### Key Insights

![Key Insights](screenshots/key_insights.png)

### Data Validation

![Data Validation Summary](screenshots/data_validation.png)

### Power Query Transformation

![Power Query Transformation](screenshots/power_query_transformation.png)

## Repository Structure

```text
Payroll-Analytics-Project/
├── README.md
├── data/
├── documentation/
├── excel/
│   └── NYC_Payroll_Analysis_2025.xlsx
└── screenshots/
    ├── nyc_overtime_dashboard.png
    ├── key_insights.png
    ├── data_validation.png
    └── power_query_transformation.png
```

## Limitations

- Findings cover only the three selected agencies, not all New York City agencies.
- The analysis is descriptive and does not establish the causes of overtime differences.
- Flagged records require further review before being treated as errors.
- Payroll record counts are not equivalent to unique employee counts.
- Power Query source file paths may need updating when the workbook is opened on another computer.

## Future Improvements & AI Integration

Future enhancements could expand this analysis beyond descriptive reporting through:

- **Predictive Analytics:** Apply Python and machine learning to forecast overtime spending using historical payroll trends.
- **Anomaly Detection:** Identify unusual overtime payments and potential data-quality issues using statistical or machine learning techniques.
- **AI-Assisted Reporting:** Explore generative AI and Power BI automation to streamline reporting and communicate key findings to stakeholders.
