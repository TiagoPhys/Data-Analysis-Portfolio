# Data Analysis Portfolio

I'm Tiago, a data analyst based in Dublin with a PhD in Physics. My research was in stochastic processes and Monte Carlo simulation. These projects apply the same habits to business data: check the data carefully, test whether a pattern is real, and finish with a clear recommendation.

**Tools:** Python (pandas, NumPy, SciPy, scikit-learn, XGBoost, LightGBM, matplotlib, seaborn), SQL, Power BI, Looker Studio

## Projects

| # | Project | Skills | Main result |
|---|---|---|---|
| 1 | [Fraud Detection in Mobile Money](01-fraud-detection-paysim) | Classification on 6.3M imbalanced transactions, leakage control, model comparison | XGBoost reached ROC AUC 0.956, but caught only 17% of frauds at the default threshold |
| 2 | [Retail Customer Analytics: Chips Category](02-retail-customer-analytics-quantium) | Customer segmentation, hypothesis testing, brand and pack size affinity | Three segments drive sales; one of them pays significantly more per packet (Welch t-test, p < 0.001) |
| 3 | [Content Popularity on a Social Media Platform](03-social-media-content-analysis-accenture) | Joining 3 tables, cleaning category labels, client presentation | Top 5 categories by engagement; inconsistent labels had changed the ranking |
| 4 | [Data Quality Assessment for a Bike Retailer](04-data-quality-assessment-kpmg) | Data quality audit with an issue log | 17 issues across 6 quality dimensions, each with a proposed fix |
| 5 | [HR and Clients Dashboard in Power BI](05-hr-clients-dashboard-powerbi) | Dashboard design, KPIs, map visuals | 3-page report on contracts, clients and employees |
| 6 | [Loan Approval Prediction](06-loan-approval-prediction) | Leakage checks, model comparison, interpretation, threshold choice | ROC AUC 0.97 with Logistic Regression; income and loan amount drive approval |

Projects 2, 3 and 4 use case studies from the Quantium, Accenture and KPMG virtual experience programmes on Forage. The analysis and code are my own.

## How to run

```bash
git clone https://github.com/TiagoPhys/Data-Analysis-Portfolio.git
cd Data-Analysis-Portfolio
pip install -r requirements.txt
jupyter lab
```

Projects 2, 3 and 4 include their data. The fraud dataset (about 470 MB) is available on [Kaggle](https://www.kaggle.com/datasets/ealaxi/paysim1) and should be saved in `01-fraud-detection-paysim/`.

## Contact

tiago.phys@gmail.com
