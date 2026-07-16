# Telco CRM Analytics: Customer Churn & Revenue Risk

**SQL (DuckDB) + Power BI project analyzing 7,032 telco customers to quantify the
revenue impact of churn and identify the exact conditions driving it.**

## Summary

- Churn rate: **26.6%** (1,869 of 7,032 customers)
- Revenue lost to churn: **$2.86M**
- Highest-risk segment identified: month-to-month contract + Fiber Optic +
  Electronic Check payment → **60.4% churn rate**, more than double the average
- Delivered a 4-tier prioritized retention roadmap for the business team

## The Problem

The dashboard was never the hard part of this project — trusting the data was.
The `Total Charges` column looked complete at a glance, but SQL validation
revealed hidden empty strings instead of true nulls. Left uncaught, that single
issue would have quietly skewed every revenue metric built on top of it. Before
asking any business question, I built a cleaned dataset (`churn_clean`) I could
actually rely on.

## Process

**1. Data validation & cleaning (SQL / DuckDB)**
Queried the raw dataset to surface hidden data quality issues, not just obvious
nulls — the empty-string case in `Total Charges` being the key catch. Produced
a cleaned, analysis-ready table before any exploration began.

**2. Exploratory analysis (SQL)**
Reframed the work from "write a query, get an output" to answering specific
business questions: Why are customers leaving? Which segments carry the most
risk? How much revenue is actually at stake?

**3. Dashboard build & cross-validation (Power BI, DAX)**
Built the executive dashboard, then found the numbers didn't initially match
the SQL output — revenue and average charges were off, and some DAX measures
behaved inconsistently. Traced it back through data types, Power Query steps,
relationships, and measures until every number reconciled with SQL. Matching
outputs was the real milestone of this project, not the visuals.

## Key Insights

| Finding | Detail |
|---|---|
| Revenue at risk | $2.86M lost to churn, out of $16.1M total revenue |
| Highest churn driver | New customers (<12 months tenure): 48.5% churn rate |
| Payment risk | Electronic Check users churn ~3x more than automatic-payment users |
| Contract risk | Month-to-month: 42.7% churn rate vs. 2.8% for two-year contracts |
| Compounding risk | Month-to-month + Fiber Optic + Electronic Check: 60.4% churn rate |

## Recommendations Delivered

1. **Priority 1:** Convert month-to-month customers to annual contracts via renewal incentives
2. **Priority 2:** Bundle Fiber Optic with Online Security to improve retention
3. **Priority 3:** Encourage Electronic Check users to adopt AutoPay
4. **Priority 4:** Launch onboarding campaigns targeting customers without Online Security

## Tools & Skills Demonstrated

`SQL` `DuckDB` `Power BI` `DAX` `Power Query` `Data Cleaning` `Data Validation`
`Churn Analysis` `Customer Segmentation` `Business Recommendations`

## Files

- `churn_clean` — cleaned dataset used for analysis
- Dashboard screenshots / `.pbix` file — [add link if included in repo]
- SQL queries — [add link to `.sql` file if included in repo]

---

📫 Questions or feedback on this analysis? Reach out on
[LinkedIn](https://www.linkedin.com/in/dauliaoktaviona) or email deviau.ok01@gmail.com
