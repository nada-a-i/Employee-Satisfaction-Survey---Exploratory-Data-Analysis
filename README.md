# Employee Satisfaction Survey - Exploratory Data Analysis

*SQL + Power BI · 3,025 Employee Records · 8 Departments · 5 Job Levels*

---

## Executive Summary

High voluntary turnover drains institutional knowledge and inflates recruitment costs, but most HR teams manage it reactively without a data-backed view of who is actually at risk. This project analyzes 3,025 employee records using SQL and Power BI to identify satisfaction drivers, segment the workforce by risk, and deliver an interactive dashboard for HR stakeholders. Key findings: 98 at-risk employees flagged (stress ≥4 and satisfaction ≤2), with 57 holding Senior or Lead roles. Work-life balance emerges as the highest-leverage intervention, producing a 2.5-point satisfaction swing. 31 percent of the workforce works overtime, each experiencing a 0.42-point satisfaction penalty on average.

---

## Business Problem

Employee turnover is expensive. Exit interviews come too late. Engagement surveys produce averages that hide real pain points. Leadership distributes resources evenly instead of targeting high-risk pockets. This analysis answers three questions HR leadership actually cares about: Who is at risk right now and where are they concentrated? What conditions drive dissatisfaction and how much does each one matter? Where should we intervene first for the fastest return on retention investment?

---

## Methodology

SQL was used to run 12 exploratory queries covering satisfaction distribution, department and job-level comparisons, factor testing across stress, work-life balance, overtime, sleep, and commute, and at-risk segmentation. Power BI handled visualization for a non-technical HR audience, with each visual chosen based on the story it needed to tell.

<img width="1237" height="455" alt="Screenshot 2026-05-01 162953" src="https://github.com/user-attachments/assets/4e6a7cc0-d261-467f-9826-4b719511f414" />




---

## Skills Used

| Tool | Technical Techniques |
|------|---------------------|
| **SQL** | Conditional aggregation with `CASE WHEN`, `UNION ALL` for multi-factor comparisons, `GROUP BY` across multiple dimensions, `ORDER BY` sorting, percentage calculations, compound `WHERE` filters |
| **Power BI** | KPI cards, line charts, column charts, doughnut charts, drill-down tables, interactive slicers (department, job level, employment type) |

---

## Results and Recommendations

Work-life balance is the highest-leverage intervention: employees rating it at 5 averaged 4.5 satisfaction versus 2.0 for those rating it at 1. Senior talent faces disproportionate risk, with 4.68 percent of Senior and 4.57 percent of Lead employees meeting at-risk criteria. IT and Finance are systemic problems, accounting for 44 percent of at-risk employees, pointing to workload or resource allocation issues requiring department-level audit. Overtime affects 31 percent of the workforce with a 0.42-point satisfaction penalty per person.

<img width="1014" height="573" alt="Screenshot 2026-04-30 225653" src="https://github.com/user-attachments/assets/81f041b1-f697-4af7-b501-072b2bdaa6d9" />

---

## Next Steps

This snapshot analysis identifies current risk but cannot predict future turnover. A predictive retention model using logistic regression or gradient boosting trained on labeled turnover data would shift output from descriptive to prescriptive. Longitudinal tracking by quarter, manager-level segmentation, compensation data integration, and live HRIS connectivity would strengthen future iterations. The dataset currently lacks tenure data, limiting the ability to distinguish short-term dissatisfaction from chronic disengagement.

---

*SQL queries, Power BI file, and dataset included in this repository.*
