# Operational Reporting Automation & Business Analytics

**Supporting project · Excel Power Query + Power BI · Synthetic data**

A repeatable reporting workflow that turns an inconsistent activity tracker into a validated analytical dataset, operational KPIs, and an overdue action list.

**Demonstrated snapshot:** 750 activities · 338 overdue · 44 records with primary data-quality issues.

[Open the Power BI report](03_PowerBI/operations_reporting_dashboard.pbix) · [Open the Power Query workbook](02_PowerQuery/operations_reporting_cleaning.xlsx) · [Read the findings](05_Documentation/key_findings.md)

![Operational reporting dashboard with overdue workload, schedule status and action list](04_Images/dashboard_screenshot.png)

## Business Problem

Operational trackers mix incomplete updates, inconsistent categories, duplicate IDs, and invalid dates. Management needs a dependable view of overdue work and departmental risk without allowing questionable source records to distort the reporting.

## Solution

```text
Raw CSV → Excel Power Query → cleaning and standardization
→ validation and calculated fields → clean CSV
→ Power BI and DAX → dashboard → insights and follow-up priorities
```

## Data

The [raw dataset](01_Data/Raw/operations_raw.csv) contains **750 synthetic activities across six departments**. The saved report uses the cutoff **22 August 2026**. No confidential employer or client data is used.

The [cleaned dataset](01_Data/Cleaned/operations_clean.csv) preserves source activity IDs and adds a unique `Record ID`, date checks, cleaned actual-finish dates, cycle time, delay, aging, overdue flags, and data-quality classifications. Six records are marked as affected by duplicated source IDs; this is separate from the 44 primary data-quality issues.

## Analysis

- Completion, overdue workload, completed-work delay, and aging of open activities.
- Departmental backlog volume and proportional overdue exposure.
- High/Critical-priority overdue work and records requiring validation review.
- An overdue action list with department, responsible team, priority, dates, and aging.

## Decision Support

Construction has the largest overdue backlog (**87 activities**). Procurement has the highest proportional overdue exposure (**39 of 77 activities, approximately 50.6%**). These findings support separate workload and performance reviews.

The [findings](05_Documentation/key_findings.md) recommend prioritizing **153 High/Critical overdue activities**, escalating aging work, and resolving source-data issues before using affected dates in performance measures.

## Automated Action

Power Query applies repeatable preparation and validation steps; Power BI presents the resulting metrics and action list. The saved workflow includes a cleaned CSV handoff. Refreshing the workbook, exporting the cleaned table, and refreshing the report are user-run steps; unattended scheduling and automatic task assignment are not demonstrated.

## Measured / Demonstrated Outcome

| Measure | Saved snapshot |
|---|---:|
| Activities / completed | 750 / 412 |
| Completion rate | 54.9% |
| Overdue activities | 338 |
| Average delay among late completed activities | Approximately 9.6 days |
| Average aging among open activities | Approximately 121.5 days |
| Primary data-quality issues | 44 records |

The primary issue categories contain 30 invalid actual-date sequences, 8 missing priorities, and 6 missing descriptions. Additional date-check and duplicate flags remain inspectable in the cleaned data. These are demonstration results, not measured client savings or productivity gains.

## Tools

Microsoft Excel, Power Query, Power BI, DAX, and CSV files.

## How to Run

1. Download the repository and open the [Excel workbook](02_PowerQuery/operations_reporting_cleaning.xlsx) in Excel with Power Query support.
2. In Power Query, update the source path to your local [raw CSV](01_Data/Raw/operations_raw.csv), then refresh and inspect the validation fields.
3. Export the refreshed `operations_clean` table to the [cleaned CSV location](01_Data/Cleaned/operations_clean.csv), retaining its headers.
4. Open the [Power BI file](03_PowerBI/operations_reporting_dashboard.pbix) in Power BI Desktop, update its source path to the local cleaned CSV, and refresh. Keep the documented reporting cutoff to compare with the saved snapshot.

The committed workbook, report, screenshot, and findings can also be reviewed directly without refreshing the data.

---

[Portfolio overview](https://github.com/23-06109#selected-projects) · [LinkedIn](https://www.linkedin.com/in/jimmyjrmanalon)
