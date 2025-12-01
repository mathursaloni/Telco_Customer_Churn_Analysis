# Personal_Project-2
This project analyses customer churn in a telecom dataset using Python, Pandas, Seaborn and Matplotlib.   The goal is to understand which customer segments are most at risk of churn and translate those findings into concrete business recommendations.

## 1. Project Overview

- Overall churn rate of the customer base is **≈ 26.5%** (around **1 in 4 customers** leaves).
- Churn is not meaningfully driven by gender, but is **higher among senior citizens**, early-tenure customers, and those on **month-to-month contracts**.
- Internet service mix, add-on services (OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport) and **payment method (Electronic Check)** are strong signals of churn risk.
- The project combines:
  - Data cleaning and exploratory data analysis (EDA)
  - Visualisation of churn across multiple dimensions
  - An **executive summary** and **business recommendations** for retention.

For the detailed narrative, see [`docs/TCA_Executive Summary.md`](docs/TCA_Executive_Summary.md).

---

## 2. Repository Structure

```text
.
├─ data/
│   └─ telco_customer_churn_raw.csv       # source dataset
├─ notebooks/
│   └─ telco_customer_churn.ipynb         # main analysis notebook
├─ src/
│   └─ churn_analysis.py                  # (optional) reusable code
├─ docs/
│   └─ executive_summary.md               # written insights & recommendations
├─ images/                                # exported visualisations
│   ├─ churn_overall.png
│   ├─ churn_by_contract.png
│   └─ churn_by_services.png
└─ README.md
