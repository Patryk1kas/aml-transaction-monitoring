# AML Transaction Monitoring — Detecting Suspicious Activity Patterns

## Overview

This project analyses 5 million financial transactions to identify 
patterns associated with money laundering. Using IBM's synthetic 
AML dataset, I explored transaction amounts, timing, payment formats 
and daily trends to understand what makes a transaction suspicious.

This mirrors the real challenge faced by compliance analysts at banks 
and financial institutions every day — finding 5,000 suspicious 
transactions in a dataset of 5 million.

---

## Business Question

> In a dataset where only 0.10% of transactions are flagged as 
> suspicious — can we identify meaningful patterns that separate 
> laundering activity from legitimate transactions?

---

## Tools Used

| Tool | Purpose |
|------|---------|
| Python | Main analysis language |
| pandas | Data cleaning and manipulation |
| Matplotlib | Chart building and formatting |
| Seaborn | Chart styling and visualisation |
| Jupyter Notebook | Analysis environment |

---

## Data Source

- **IBM Transactions for Anti-Money Laundering (AML)**
- Downloaded via Kaggle
- 5,078,345 transactions across September 2022
- 0.10% flagged as suspicious — 5,177 transactions

🔗 [Kaggle Dataset](https://www.kaggle.com/datasets/ealtman2019/ibm-transactions-for-anti-money-laundering-aml)

---

## Project Structure

aml-transaction-monitoring/
├── data/
│   └── raw/                         # Original downloaded data
├── notebooks/
│   └── aml_analysis.ipynb          # Main analysis notebook
├── outputs/
│   └── charts/                     # All saved chart images
│       ├── 01_amount_distribution.png
│       ├── 02_activity_by_hour.png
│       ├── 03_payment_format.png
│       └── 04_daily_suspicious_trend.png
├── README.md
└── requirements.txt

---

## Key Findings

**Chart 1 — Transaction Amount Distribution**
Suspicious transactions are heavily concentrated at higher values 
while normal transactions are more spread out across a wider range. 
Suspicious transactions average $36M compared to $4.4M for normal 
transactions — an 8x difference.

**Chart 2 — Activity by Hour of Day**
Suspicious activity peaks during business hours, particularly around 
midday at 6.5% of daily volume. This suggests sophisticated laundering 
deliberately timed to blend in with legitimate transaction flow.

**Chart 3 — Payment Format Breakdown**
ACH transfers account for 86.6% of all suspicious transactions despite 
only making up 11.8% of normal activity. Contrary to popular assumption, 
Bitcoin accounts for just 1.1% of suspicious transactions.

**Chart 4 — Daily Suspicious Transaction Trend**
Suspicious activity built gradually to a peak of 539 transactions on 
September 8th before declining sharply — consistent with a coordinated 
laundering campaign that either got detected or concluded.

---

## Conclusion

Money laundering does not always look the way you expect. It hides 
in plain sight — using mainstream payment methods, operating during 
business hours, and moving large amounts that individually might not 
trigger automated rules. The value of data analysis in AML is 
connecting those dots before the money disappears.

---

## How to Run

1. Clone the repository
```bash
git clone https://github.com/Patryk1kas/aml-transaction-monitoring.git
```

2. Install dependencies
```bash
pip install -r requirements.txt
```

3. Open the notebook
```bash
cd aml-transaction-monitoring
jupyter notebook
```

4. Navigate to `notebooks/aml_analysis.ipynb` and run all cells

---

*Data source: IBM Synthetic AML Dataset via Kaggle*