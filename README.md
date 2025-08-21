# GCC Analytics Dashboard – Power BI

## Overview

This project is a **Global Capability Centre (GCC) Analytics Dashboard** built in **Power BI**. It provides insights into headcount, attrition, training, operating costs, client satisfaction, and compliance across GCC locations. The dashboard includes **interactive visuals, What-If scenarios, and optional row-level security** to enable data-driven decision-making.

## Features

**Key Metrics**:

  * Total Headcount
  * Average Attrition Rate %
  * Total Training Hours
  * Average Client Satisfaction %
  * Total Operating Cost
  * YoY Headcount Change

  **What-If Scenario Analysis**:

  * Attrition Reduction % (0–10%, step 0.5)
  * Cost per Attrition (USD 1,000–15,000, step 500)
  * Calculates **Adjusted Attrition Rate**, **Attrition Cost**, and **Savings** dynamically

 **Polished Dashboard**:

  * Conditional formatting for Compliance Score and Client Satisfaction
  * Tooltips with sparklines
  * Reset filters button
  * Flat month axis using Date column

  **Optional Advanced Features**:

  * Row-Level Security (RLS) by Region
  * Automatic folder ingestion using Power Query (M)

## Getting Started

### Requirements

* Power BI Desktop (latest version)
* Power BI Pro or Premium Per User (for sharing internally)
* Sample dataset (CSV files for each month)

### Installation / Setup

1. Clone or download the repository.
2. Open the Power BI `.pbix` file.
3. Connect to your dataset (or folder of CSV files).
4. Verify relationships between **fact\_gcc\_ops\_monthly**, **dim\_date**, and **dim\_gcc** tables.
5. Create What-If parameters (already included if using the provided `.pbix`).
6. Apply bookmarks, conditional formatting, and tooltips as needed.


## Dashboard Insights (Storytelling)

* APAC centres lead headcount growth but also show higher attrition. Training & automation correlate with improved success rates.
* Compliance improvements are associated with fewer audit findings; EMEA sites show the strongest compliance maturity.
* A **3% attrition reduction scenario** yields **\$X savings** (see What-If page).


## Troubleshooting

| Issue                  | Fix                                                                           |
| ---------------------- | ----------------------------------------------------------------------------- |
| Can’t mark date table  | Ensure `dim_date[Date]` is Date type and continuous. Then mark as date table. |
| Line charts jump       | Use `dim_date[YearMonth]` and sort by `MonthNo`.                              |
| Blank visuals          | Check relationships and slicers/filters.                                      |
| Totals wrong           | Use explicit measures.                                                        |
| Drillthrough confusing | Add a Drillthrough button.                                                    |

## License

This repository is for **educational**. Do not use sensitive data when publishing publicly.

