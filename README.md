# Project Progress KPI Dashboard

**Supporting project · Excel + Power BI · Data → KPI Visibility**

Turns a 20-activity project tracker into a view of planned versus actual progress, activity status, and discipline-level schedule gaps.

**Demonstrated finding:** average actual progress is **38.25%** against **52.5%** planned, a **14.25 percentage-point shortfall**.

[Open the Excel workbook](Project_Progress_KPI_Dashboard.xlsx) · [Open the Power BI report](Project_Progress_KPI_Dashboard_PowerBI.pbix)

![Project progress dashboard showing planned versus actual progress and activity status](powerbi-dashboard.png)

## Business Problem

Project teams need a consolidated view of execution against plan. A row-by-row tracker makes it harder to see which disciplines are behind and where follow-up is needed.

## Solution

Excel Power Query prepares the tracker for formulas, PivotTables, and PivotCharts. Power BI presents KPI cards, planned/actual comparisons, activity status, and an interactive discipline slicer.

## Data

The workbook contains 20 activity records with discipline, responsible team, planned and actual dates, progress percentages, and status. Its `Raw_Data` and `qry_ProjectProgress_Clean` sheets make the inputs and transformations inspectable.

The records are **synthetic/demo data**, as confirmed by the project author. Results demonstrate the reporting approach and are not employer or client outcomes.

## Analysis and Decision Support

| Measure | Saved result |
|---|---:|
| Total activities | 20 |
| Completed / In Progress / Delayed / Not Started | 2 / 7 / 3 / 8 |
| Average planned progress | 52.5% |
| Average actual progress | 38.25% |
| Average progress variance | −14.25 percentage points |

Managers can compare discipline-level gaps, review delayed activities, and focus recovery discussions on work behind plan. These progress percentages are simple activity averages, not effort- or cost-weighted project completion.

## Automated Action

Power Query, formulas, and PivotTables support repeatable preparation and summary reporting when refreshed. The project demonstrates reporting visibility; automated escalation or task updates are not implemented.

## Measured / Demonstrated Outcome

The saved analysis exposes the 14.25 percentage-point planned/actual gap. It does not measure a subsequent improvement in delivery.

**Interpretation note:** the saved dashboard's “Completed Late” value of 2 counts records with an actual finish after the planned finish. One of those records remains marked Delayed with 90% progress in the source. Read this as a date-based late-finish count, not two status-confirmed completed-late activities.

## Tools and Outputs

Excel, Power Query, Excel formulas, PivotTables/PivotCharts, Power BI Desktop, DAX, and interactive slicers.

The [Excel workbook](Project_Progress_KPI_Dashboard.xlsx) includes raw data, cleaned data, pivot analysis, a dashboard, and a project summary. The [Power BI file](Project_Progress_KPI_Dashboard_PowerBI.pbix) provides the interactive report; the [screenshot](powerbi-dashboard.png) provides a quick preview.

## How to Run

1. Download the repository. Open the Excel workbook and start with `Dashboard` or `Project_Summary`.
2. Inspect `Raw_Data` and the Power Query steps before refreshing. Update any source path to your local copy if prompted, then refresh the queries and PivotTables.
3. Open the `.pbix` file in Power BI Desktop. Update its source connection to your local workbook if needed and refresh. Use the discipline slicer to explore the saved report.

This project provides the KPI visibility foundation for the later SQL analysis and reporting automation projects in the portfolio.

---

[Portfolio overview](https://github.com/23-06109#selected-projects) · [LinkedIn](https://www.linkedin.com/in/jimmyjrmanalon)
