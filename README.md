# Customer Churn Prediction

A binary classification experiment using the Telco Customer Churn dataset. The target is whether a customer churned (`Yes` / `No`).

## Dataset

- File: `WA_Fn-UseC_-Telco-Customer-Churn.csv`
- Target: `Churn`
- `customerID` is excluded from model features.
- `TotalCharges` is converted to numeric and invalid target/charge rows are excluded.

Verify the dataset's original source and redistribution license before publishing or reusing it.

## Setup

Python 3.10+:

```bash
python -m venv .venv
# Windows PowerShell: .venv\Scripts\Activate.ps1
# macOS/Linux: source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python train.py
```

## Methodology

The script uses stratified train/validation/test splits, compares multiple classifiers, evaluates decision thresholds on validation data, and reports final test metrics. Class imbalance is considered through class weighting and threshold selection. Outputs include per-threshold validation results and model comparison CSVs.

## Metrics and responsible interpretation

Accuracy alone is insufficient for churn detection. Review precision, recall, F1 and ROC-AUC, and choose an operating threshold based on the business cost of false positives and false negatives. Do not claim that higher recall is automatically better without considering intervention cost and customer impact.

The current script includes an exploratory first model comparison and a tuned follow-up section in one execution. Treat the final output as an experiment, not a production-ready churn system. Record the dataset version and actual run results.

## Privacy

Use only appropriately licensed or synthetic customer data. Never commit real customer records or personal identifiers.

## License

No license is declared. All rights reserved unless the repository owner adds an explicit license.
