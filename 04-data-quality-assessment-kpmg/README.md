# Data Quality Assessment — Bike Retailer

**Notebook:** [`data_quality_assessment.ipynb`](data_quality_assessment.ipynb)

## Problem
Sprocket Central, a bike retailer, wants to target high-value customers. Before modelling, the client asked for an **assessment of its data quality** and **recommendations to fix it**. Data: transactions (20k), customer demographics (4k) and addresses (4k). *(Case study from the KPMG virtual experience programme.)*

## Approach
Each table was checked against six data-quality dimensions — **completeness, consistency, accuracy, validity, integrity, relevancy** — and every issue was logged with the rows affected and a recommended fix, instead of silently dropping data.

![Missing values](images/missing_values.png)

## Key findings
17 issues logged, including:
- **Completeness:** 16% of customers without industry, 13% without job title; 197 transactions missing all product details.
- **Consistency:** mixed codes for gender (`F` / `Femal` / `Female`) and state (`NSW` / `New South Wales`).
- **Accuracy:** a customer born in 1843; a `default` column full of garbage strings; a typo (`Argiculture`).
- **Integrity:** a customer ID in transactions with no customer record; demographic and address tables don't fully match.
- **Relevancy:** cancelled orders and deceased customers that must be excluded from targeting.

![Issues by dimension](images/issues_by_dimension.png)

## Recommendations
Controlled vocabularies (dropdowns) at data entry, validation rules for dates, synchronised keys across systems, and removal of unusable fields at source. The notebook ends by applying all fixes to produce analysis-ready tables.
