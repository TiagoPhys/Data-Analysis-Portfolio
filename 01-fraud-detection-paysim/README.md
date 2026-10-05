# Fraud Detection in Mobile Money Transactions

**Notebook:** [`fraud_detection.ipynb`](fraud_detection.ipynb)

## Problem
Detect fraudulent transactions in a mobile-money system where fraud is extremely rare (0.13% of 6.3M transactions). Data: [PaySim](https://www.kaggle.com/datasets/ealaxi/paysim1), a synthetic dataset built from real mobile-money logs.

## Approach
1. **EDA** — distribution of amounts (log scale), fraud by transaction type and by origin → destination.
2. **Feature engineering** — derived the transaction direction (customer→customer, customer→merchant) from account IDs, then dropped the IDs to avoid memorisation.
3. **Leakage control** — removed the balance columns: fraudulent transactions are cancelled in the simulation, so balances reveal the label.
4. **Modelling** — stratified 70/30 split; compared Logistic Regression, Random Forest, LightGBM and XGBoost.

## Key findings
- All fraud happens in **TRANSFER** and **CASH_OUT** transactions between two customer accounts; a transfer is ~4x more likely to be fraud than a cash-out.

  ![Transactions and fraud rate by type](images/transactions_by_type.png)

- **XGBoost ranks best (ROC AUC 0.956)**, but at the default threshold it catches only 17% of frauds with 92% precision. With such imbalance, the decision threshold has to be set by the cost of a missed fraud vs. a false alarm.

  ![ROC curves](images/roc_curves.png)

| Model | Precision (fraud) | Recall (fraud) | ROC AUC |
|---|---|---|---|
| XGBoost | 0.92 | 0.17 | **0.956** |
| Random Forest | 0.72 | **0.35** | 0.794 |
| LightGBM | 0.59 | 0.20 | 0.886 |
| Logistic Regression | 0.18 | 0.00 | 0.901 |

## Next steps
PR-AUC and precision–recall curves, threshold tuning to a target recall, class weighting, time-based validation, and behavioural features (hour of day, velocity per account).

## Run it
Download the CSV from Kaggle into this folder, then run the notebook. Libraries: see [`requirements.txt`](../requirements.txt).
