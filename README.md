# Exploretory Data Analysis - Employee Satisfaction Survey

A comprehensive exploratory data analysis of 3,025 employee records uncovering satisfaction drivers, retention risks, and actionable HR interventions.

---

## 🎯 Project Overview

This EDA investigates a critical HR question: **Why are employees leaving, and what levers move satisfaction?**

Using SQL exploratory queries and Power BI visualization, this analysis:
- **Segments** 3,025 employees across 8 dimensions (department, job level, overtime, etc.)
- **Tests hypotheses** about satisfaction drivers (stress, workload, WLB, sleep)
- **Identifies at-risk populations** (98 employees with high stress + low satisfaction)
- **Quantifies impact** of each factor on overall satisfaction
- **Recommends interventions** with data-backed ROI

**Result:** A strategic HR dashboard enabling targeted retention efforts.

---

## 📊 Dashboard Screenshot

<img width="1014" height="573" alt="Screenshot 2026-04-30 225653" src="https://github.com/user-attachments/assets/95212526-1983-45c9-a47a-8404cb4cf910" />

---

## 🔍 EDA Findings

### Discovery 1: Satisfaction Distribution is Skewed (But Concerning)
- 58% of employees are satisfied (scores 4-5)
- 23% are dissatisfied (scores 1-2)
- **Gap:** While majority is satisfied, 700+ employees are actively disengaged

### Discovery 2: At-Risk Population is Concentrated
- **98 employees (3.2%)** meet at-risk criteria (Stress ≥4 AND Satisfaction ≤2)
- **Concentration:** IT (23) and Finance (21) account for 44% of at-risk population
- **Severity:** 57 at-risk employees are Senior/Lead roles—critical talent loss

### Discovery 3: Work-Life Balance is the Dominant Driver
| WLB Score | Avg Satisfaction | Impact |
|-----------|------------------|--------|
| 5 (Excellent) | 4.5 | ← High performers |
| 3 (Neutral) | 3.2 | ← Baseline |
| 1 (Poor) | 2.0 | ← At-risk zone |
| **Differential** | **2.5 points** | **Largest driver** |

Work-Life Balance shows a **2.5-point satisfaction differential**—the largest impact across all tested factors (stress, workload, sleep).

### Discovery 4: Stress Shows Inverse Relationship
Stress level → Average Satisfaction
- Stress 1: 3.82 satisfaction
- Stress 2: 3.45 satisfaction
- Stress 3: 2.89 satisfaction
- Stress 4: 2.10 satisfaction
- Stress 5: 1.80 satisfaction

**Pattern:** Clear downward trend. High stress = low satisfaction (inverse correlation).

### Discovery 5: Overtime Carries Hidden Cost
Employees with overtime vs without:
- **Satisfaction:** 3.10 vs 3.52 (0.42-point loss)
- **WLB score:** 3.00 vs 3.09 (measurable decline)
- **Sleep hours:** 7.03 vs 7.00 (minimal difference, surprisingly)
- **Population affected:** 936 employees (31% of workforce)

**Insight:** Overtime is a satisfaction tax affecting nearly one-third of the workforce.

### Discovery 6: Senior Leaders Show Disproportionate Risk
By job level at-risk count:
- Senior: 41 employees (4.68% of Senior cohort) ← **Highest % at-risk**
- Lead: 16 employees (4.57% of Lead cohort)
- Mid: 21 employees (2.33% of Mid cohort)
- Junior: 16 employees (2.46% of Junior cohort)
- Intern/Fresher: 4 employees (1.60% of Intern cohort)

**Critical finding:** Your most experienced talent is proportionally at highest risk.

---

## 📈 Analysis Methodology

### Exploratory Queries (12 total)
1. **Satisfaction distribution** — Understand baseline sentiment
2. **Department comparison** — Identify performance gaps
3. **Factor testing** (stress, WLB, workload, sleep) — Hypothesis testing via CASE WHEN aggregation
4. **At-risk segmentation** — Define and quantify risk
5. **Overtime impact** — Measure behavioral correlations
6. **Job level analysis** — Cohort comparison
7. **Commute/training** — Secondary factors

### SQL Techniques Applied
- **Conditional aggregation** (CASE WHEN) to test factor impacts
- **UNION ALL** to stack multi-factor comparisons
- **GROUP BY** across dimensions (Dept, JobLevel, haveOT)
- **Percentage calculations** for context
- **Custom sorting** (CASE in ORDER BY) for logical ordering

### Visualization Strategy
- **KPI cards** for executive metrics (baseline, at-risk count)
- **Line charts** for factor impact trends (stress, WLB show opposing curves)
- **Column charts** for distribution and department ranking
- **Doughnut** for job level composition
- **Table** for drill-down into individual at-risk employees
- **Text box** for prioritized recommendations

---

## 🎬 Key Recommendations

**URGENT:** Retain 41 Senior leaders at-risk by implementing executive coaching and burnout prevention programs. This cohort represents 4.68% at-risk rate—critical talent loss exposure requiring immediate intervention.

**URGENT:** Conduct IT Department audit immediately. 23 employees at-risk (2.97% of IT workforce) indicates systemic workload or process issues. Prioritize automation opportunities and resource rebalancing.

**HIGH:** Launch Work-Life Balance initiative as primary satisfaction lever. Employees rating WLB 5/5 average 4.5 satisfaction versus 1-2 for those rating 1/5—a 2.5-point differential, the largest driver across all factors.

**HIGH:** Implement overtime reduction program targeting <20% population (currently 31%). Each overtime employee shows 0.42-point satisfaction loss, affecting 936 employees. Flexible scheduling and workload distribution yield measurable ROI.

Review Finance Department resource allocation and deadline pressures. 21 at-risk employees (3.3% of Finance) suggest capacity constraints. Consider staffing or process streamlining.

Equalize training investment across job levels. Junior staff receive 6% fewer training hours than Senior roles, correlating with lower satisfaction. Development pathways strengthen retention.

---

## 📋 Dashboard Features

**Interactive Filters (Left Panel):**
- Department (8 options)
- Job Level (Intern/Fresher, Junior, Mid, Lead, Senior)
- Employment Type (Full-Time, Part-Time, Contract)

**Core Visuals:**
- **Satisfaction Distribution** (column chart) — Shows 58% satisfied, 23% dissatisfied
- **Stress/Workload/WLB Impact** (line chart) — Reveals WLB as dominant driver
- **Training Hours by Level** (doughnut) — Shows investment distribution
- **High Performers at Risk** (table) — Drill-down into individual employees
- **Insights & Recommendations** (text) — Prioritized action items

---

## 📁 Analysis Workflow

<img width="1237" height="455" alt="Screenshot 2026-05-01 162953" src="https://github.com/user-attachments/assets/684e7f9b-788b-445d-a979-9552385b4879" />


---

## 📊 Data Source

- **File:** employeesurvey.csv
- **Records:** 3,025 employees
- **Dimensions:** 8 departments, 5 job levels, 3 employment types
- **Metrics:** Satisfaction (1-5), Stress (1-5), WLB (1-5), Overtime status, Training hours, Sleep hours, Commute mode/distance, Team size, Experience
- **Time period:** Point-in-time snapshot

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| **SQL** | Data aggregation, hypothesis testing, factor impact quantification |
| **Power BI** | Dashboard design, interactive visualization, drill-down capability |
---

## 🚀 How to Use This Analysis

### For HR Leadership
1. Open the dashboard
2. Filter by your department or job level
3. Review the "Insights & Recommendations" section
4. Focus on URGENT items first (Senior retention, IT/Finance audits)

### For Data Analysts
1. Review `SQL_Queries.md` for complete methodology
2. Examine conditional aggregation patterns (CASE WHEN)
3. Test additional hypotheses using the provided queries as templates
4. Consider extending with predictive retention scoring

---
