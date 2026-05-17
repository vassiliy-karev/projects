# PaySim — Mobile Money Transaction Analysis

Exploratory analysis and fraud detection on the PaySim synthetic mobile money dataset. This repo is part of my portfolio and walks through the full workflow: loading a realistic, imbalanced transactional dataset, profiling it, engineering features, and building a baseline fraud classifier.

## Problem statement

Mobile money platforms process millions of peer-to-peer transactions daily. A small fraction are fraudulent — typically account takeovers where an attacker drains a balance through `TRANSFER` and `CASH_OUT` chains. The business problem is to flag suspicious transactions in near-real-time without flooding the review queue with false positives.

This project treats it as a binary classification problem on a heavily imbalanced dataset (~0.13% positive class), with emphasis on:

- Honest evaluation under class imbalance (precision/recall at operating thresholds, not just accuracy)
- Feature engineering grounded in transaction semantics, not just statistical tricks
- Reproducibility — anyone with a Kaggle account should be able to clone this and rerun end-to-end

## Dataset

**Source:** [PaySim1 on Kaggle](https://www.kaggle.com/datasets/ealaxi/paysim1) (Lopez-Rojas, 2016)

PaySim is a synthetic dataset generated from a real mobile money service operating in an African country. The simulator reproduces normal transaction behavior and injects fraudulent agents. Roughly 6.4M rows over 30 simulated days, ~470MB uncompressed.

Key characteristics:

- **5 transaction types:** `CASH_IN`, `CASH_OUT`, `DEBIT`, `PAYMENT`, `TRANSFER`
- **Fraud concentrated in 2 types:** only `TRANSFER` and `CASH_OUT` contain fraudulent transactions
- **Severe class imbalance:** 8,213 fraud cases out of 6,362,620 (~0.129%)
- **Built-in rule flag:** an `isFlaggedFraud` column that fires on transfers over 200,000 — useful as a naive baseline

Full schema and column-by-column notes are in [`data/schema.md`](data/schema.md).

## Repository structure

```
.
├── README.md
├── requirements.txt
├── .gitignore
├── data/
│   ├── schema.md          # column definitions, types, gotchas
│   └── *.csv              # gitignored — pull from Kaggle (see below)
└── notebooks/
    └── 01_sql_exploration.ipynb
```

## Getting the data

The CSV is gitignored because of its size. To pull it locally:

1. Install the Kaggle CLI and configure credentials (see [Kaggle API docs](https://github.com/Kaggle/kaggle-api#api-credentials))
2. From the repo root:

```bash
pip install -r requirements.txt
kaggle datasets download -d ealaxi/paysim1 --unzip -p data/
```

You should end up with `data/PS_20174392719_1491204439457_log.csv` (~470MB).

## Roadmap

- [x] Repo skeleton, README, schema documentation
- [x] SQL exploration notebook scaffold — 5 first-pass questions ready to run
- [ ] EDA notebook — distributions, transaction-type breakdowns, fraud signatures
- [ ] Feature engineering — balance-delta features, origin/destination patterns
- [ ] Baseline models — logistic regression, gradient boosting
- [ ] Evaluation — PR curves, threshold tuning, cost-sensitive analysis
- [ ] Writeup — short post summarizing findings

## Tech stack

Python, pandas, scikit-learn, matplotlib/seaborn, Jupyter. Kept intentionally minimal — the point is the analysis, not the infrastructure.

## Notes

This is a learning and portfolio project. The dataset is synthetic, so any "fraud detector" trained on it won't generalize to real payments traffic — but the workflow, the evaluation discipline, and the feature engineering patterns do transfer.
