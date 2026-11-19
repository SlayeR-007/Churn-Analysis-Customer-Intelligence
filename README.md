# Churn Analysis & Customer Intelligence

**Data Analytics Project | OTT Subscription Platform**

---

## 1. The Business Challenge

In the hyper-competitive OTT landscape (Netflix, Hotstar, Prime), customer retention is essential for sustainable growth.

This project focuses on identifying high-risk subscribers using a multidimensional dataset containing:

- Customer demographics
- Subscription tiers and contract structures
- Customer support interactions and escalations

The objective is to understand customer churn patterns, quantify revenue impact, identify potential churn drivers and recommend data-driven retention strategies.

## 2. Core Tech Stack

| Category | Technologies / Skills |
|---|---|
| SQL & Python Integration | NumPy, Pandas, SQLite3 |
| Data Visualization | Matplotlib, Seaborn |
| Performance Engineering | Data Cleaning, Feature Engineering, Analytics |
| Business Intelligence | Behavioral Visualization, KPI Analysis |
| Business Communication | Actionable Insights, Executive Reporting |

## 3. Project Milestones

- **Relational Data Extraction:** Connecting Python to SQL databases to retrieve multi-table datasets.
- **Advanced Feature Engineering:** Importing data, calculating customer tenure, churn rates and customer aging.
- **Executive Reporting:** Translating technical findings into actionable business insights and recommendations.

## 4. Database Tables

**Database:** `customer_churn`

The project uses three relational tables:

### Table 1: db_customer

| Column | Description |
|---|---|
| customerid | Unique customer identifier |
| name | Customer name |
| country | Customer country |
| state | Customer state |
| gender | Customer gender |
| dob | Date of birth |
| interests | Customer interests |
| pincode | Postal code |

### Table 2: db_subscription

| Column | Description |
|---|---|
| customerid | Unique customer identifier |
| subscription_start_date | Subscription start date |
| subscription_type | Subscription acquisition/type information |
| renewal_date | Subscription renewal date |
| plan_type | Basic / Standard / Premium |
| contract_type | Monthly / Annual |
| cancellation_date | Subscription cancellation date |
| cancellation_reason | Reason for cancellation |
| monthly_charges | Monthly subscription charges |
| cltv | Customer Lifetime Value |
| churn_score | Customer churn risk score |

### Table 3: db_support

| Column | Description |
|---|---|
| customerid | Unique customer identifier |
| complaint_date | Date of customer complaint |
| Escalations | Support escalation indicator |
| csat_score | Customer satisfaction score |
| col_1 | Additional source field |
| comment | Customer support comments |

## 5. Calculated Metrics

The following KPIs are used to evaluate customer churn, retention and revenue exposure.

| KPI | Formula / Calculation |
|---|---|
| Churn Rate | Churned Customers / Total Customers |
| Churn by Plan Type | Churn Rate GROUP BY plan_type (Basic / Standard / Premium) |
| Churn by State | Churn Rate GROUP BY country, state |
| Retention Rate | 1 − Churn Rate |
| ARPU | SUM(monthly_charges) / COUNT(active customerid) |
| Average Customer Tenure | AVG(DATEDIFF(cancellation_date OR NOW(), subscription_start_date)) |
| Revenue at Risk | SUM(monthly_charges) WHERE churn_score > 70 |
| Escalation Rate | SUM(escalations) / COUNT(complaints) × 100 |
| Average Complaints per Customer | COUNT(complaints) / COUNT(DISTINCT customerid) |
| Correlation: Escalations → Churn | Churn Rate WHERE escalations ≥ 1 vs. 0 |

## 6. Key Insights

The analysis revealed the following findings:

| KPI | Result |
|---|---:|
| Churn Rate | 28.6% |
| Retention Rate | 71.4% |
| Average Customer Tenure | 1,451 days |
| ARPU | Rs 18.8 |
| Total Revenue | 395 |
| Revenue Loss Due to Churn | 74 |
| CLTV Lost | 2,047 |
| Revenue Loss Percentage | 18% |
| Monthly Contract Churn | 55.6% |
| Annual Contract Churn | 8.3% |

### Business Observations

- Most of the observed churn comes from the Basic subscription plan, with relatively limited revenue impact compared with higher-value customer segments.
- The highest number of cancellations occurred in September 2024.
- Karnataka was the most affected state.
- Monthly-contract subscribers exhibited substantially higher churn than annual-contract subscribers.
- The difference between monthly and annual contract churn indicates an opportunity to improve long-term customer retention.

## 7. Recommended Action Items

Based on the findings, the following actions are recommended:

1. **Investigate Karnataka:** Examine whether price increases, customer complaints, technical issues or service disruptions contributed to the higher churn.

2. **Review Basic Plan Pricing:** Investigate whether subscription price changes or modifications to the Basic plan, particularly around September 2024, influenced cancellations.

3. **Competitor Analysis:** Evaluate competitor offerings and pricing strategies, particularly where customers have cited switching to competitors.

4. **Prioritise High- and Medium-Risk Customers:**
   - Identify customers with High and Medium churn-risk scores.
   - Evaluate their Customer Lifetime Value (CLTV).
   - Analyse their complaint history and support requests.
   - Prioritise customers based on potential revenue impact.
   - Reach out through email, SMS and phone calls to understand and resolve their issues.

## 8. Portfolio Project Summary

### A. Churn & Revenue Impact

Engineered an end-to-end churn analytics pipeline for an OTT subscription platform by integrating multi-table subscriber data across acquisition type, contract structure and plan tier (20+ KPIs).

Uncovered a significant churn disparity between monthly and annual contract segments, quantified MRR leakage and CLTV erosion attributed to high-risk cohorts, and delivered a data-backed contract-migration retention strategy to reduce subscriber loss.

### B. Risk Scoring & Segmentation

Developed a multidimensional churn risk scoring model by synthesising subscription tenure, plan type and support escalation signals across three relational tables (20+ KPIs).

Segmented the customer base into risk tiers using composite churn scores, exposed a significant lifetime value gap between churned and retained cohorts, and recommended prioritising Premium annual-plan retention over Basic monthly acquisition to maximise long-term revenue yield.

### C. Support Intelligence & Cancellation Analysis

Performed cross-functional support–churn correlation analysis by joining complaint, escalation and CSAT data with subscription records.

Identified that escalated support interactions were disproportionately concentrated among churned customers, decomposed cancellation drivers into competitor switching, pricing sensitivity and content dissatisfaction, and translated findings into a prioritised product and pricing roadmap.

### D. Churn & Revenue Impact — Quantified Results

Engineered an end-to-end churn analytics pipeline for an OTT subscription dataset (20+ KPIs), identifying a **28.6% overall churn rate**.

Identified that monthly-contract subscribers churned at **55.6%**, which is approximately **6.7 times** the **8.3% annual-contract churn rate**.

Quantified **$73.94/month in MRR leakage** and **$2,047 in CLTV erosion** attributed to six at-risk customers, enabling a targeted contract-migration retention strategy.

---

*Data Analytics Project | Churn Analysis & Customer Intelligence*
