# Data Analysis Portfolio — Tiago

PhD in Physics turned data analyst, based in Dublin. My research background is in stochastic processes and Monte Carlo simulation; this portfolio shows how I apply the same rigour to business data — cleaning messy inputs, testing whether patterns are real, and turning results into recommendations.

**Tools:** Python (pandas, NumPy, SciPy, scikit-learn, XGBoost, LightGBM, matplotlib, seaborn) · SQL · Power BI · Looker Studio

---

## Projects

| # | Project | What it shows | Key result |
|---|---|---|---|
| 1 | [**Fraud Detection — Mobile Money**](01-fraud-detection-paysim) | Classification on 6.3M imbalanced transactions, leakage control, model comparison | XGBoost ROC AUC 0.956; analysis of why recall, not AUC, is the real challenge at 0.13% fraud |
| 2 | [**Retail Customer Analytics — Chips Category**](02-retail-customer-analytics-quantium) | Customer segmentation, hypothesis testing, brand/pack affinity | Identified 3 segments driving sales; Mainstream young singles/couples pay significantly more per unit (Welch t-test, p < 0.001) |
| 3 | [**Content Popularity — Social Media Platform**](03-social-media-content-analysis-accenture) | Data modelling across 3 tables, label cleaning, client presentation | Top 5 categories by engagement; showed that inconsistent labels changed the ranking |
| 4 | [**Data Quality Assessment — Bike Retailer**](04-data-quality-assessment-kpmg) | Systematic data-quality audit with an actionable issue log | 17 issues logged across 6 quality dimensions, each with a recommended fix |
| 5 | [**HR & Clients Dashboard — Power BI**](05-hr-clients-dashboard-powerbi) | Interactive dashboard design, KPIs, geographic view | 3-page report on contracts, clients and workforce |

Projects 2–4 are based on case studies from the Quantium, Accenture and KPMG virtual experience programmes (Forage); the analysis and code are my own.

<p align="center">
  <img src="02-retail-customer-analytics-quantium/images/segment_metrics.png" width="85%" alt="Segment analysis: sales, customers, units and price per unit by life stage and price segment">
</p>

---

## Running the notebooks

```bash
git clone https://github.com/TiagoPhys/Data-Analysis-Portfolio.git
cd Data-Analysis-Portfolio
pip install -r requirements.txt
jupyter lab
```

Projects 2–4 include their data and run end to end. The fraud dataset (~470 MB) must be downloaded from [Kaggle](https://www.kaggle.com/datasets/ealaxi/paysim1) into `01-fraud-detection-paysim/`.

## Contact

📧 tiago.phys@gmail.com
