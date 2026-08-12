SaaS Revenue & Cohort Retention Analysis
An end-to-end analysis of a SaaS company's customer cohorts, subscription revenue, and retention patterns, using Python, SQL, and Power BI.
Business Problem
Subscription businesses live and die by retention — acquiring a customer means little if they churn before their subscription value exceeds what it cost to acquire them. This project analyzes signup cohorts, monthly recurring revenue (MRR), and customer lifetime value (LTV) against acquisition cost (CAC) to answer three questions:
Is retention improving or declining across newer customer cohorts?
Is revenue growth sustainable, or is it stalling?
Which subscription plan delivers the best return on acquisition spend?
Dataset
Synthetic SaaS business dataset (Kaggle) with three related tables:
customers — signup date, plan type, monthly fee, acquisition cost, churn date
subscriptions — monthly subscription status per customer
revenue — monthly revenue transactions per customer
Key Findings
Retention is declining sharply in newer cohorts. Customers who signed up in late 2024 and early 2025 are churning much faster than earlier cohorts. For example, the 2024-11 cohort retained 85.7% of customers by month 4, while the 2025-04 cohort had already dropped to 12.5% by month 2.
Revenue growth has stalled and reversed. Monthly Recurring Revenue grew steadily from ₹4,600 (Feb 2024) to a peak of ₹22,500 (Feb 2025), then declined to ₹3,900 by June 2025 — a drop that lines up directly with the retention breakdown in newer cohorts.
Enterprise customers are the most valuable segment. The Enterprise plan generates ₹167,000 in total revenue — more than Basic and Pro combined (₹82,800) — despite having fewer customers. Enterprise also has the strongest LTV:CAC ratio at 2.53, compared to 1.95 for Pro and 1.63 for Basic.
Recommendation
The business should prioritize retention efforts on cohorts acquired from late 2024 onward, and investigate what changed in onboarding, pricing, or product experience around that period. Enterprise customers represent the best return on acquisition spend and should be a focus for both retention and targeted growth.
Tech Stack
Python (Pandas) — data cleaning, cohort construction, retention matrix calculation
SQLite — relational database and SQL querying (cohort retention, MRR aggregation)
Power BI — dashboard with MRR trend, cohort retention curve, revenue by plan, and LTV:CAC visuals
Files in this Repo
SaaS_Cohort_Analysis.ipynb — full Python analysis notebook
SaaS_Cohort_Dashboard.pbix — Power BI dashboard
customers.csv, subscriptions.csv, revenue.csv — source data
retention_pct.csv, mrr_trend.csv, revenue_by_plan.csv, ltv_cac.csv — cleaned outputs used in the dashboard
Power BI Dashboard

The Power BI dashboard provides an interactive view of SaaS revenue, cohort retention, revenue by subscription plan, and LTV:CAC performance.

![SaaS Revenue & Cohort Retention Dashboard] (SaaS_Cohort_dashboard_preview.png)

Dashboard Includes

- Monthly Recurring Revenue (MRR) trend
- Cohort retention analysis
- Revenue by subscription plan
- LTV:CAC ratio by plan type
- Overall SaaS revenue analysis
