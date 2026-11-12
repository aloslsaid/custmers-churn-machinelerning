# Customer Churn Prediction

An educational binary-classification project for predicting customer churn from the Telco Customer Churn dataset. The repository includes `WA_Fn-UseC_-Telco-Customer-Churn.csv` and a project file named `coustmer churn 11`; inspect the latter to determine whether it is a notebook, script, or another file type.

## Setup

1. Clone or download the repository.
2. Review the dataset source/license and inspect its column names, especially the target column.
3. Inspect `coustmer churn 11` for its expected Python version, entry point, and data path.
4. Create a virtual environment and install dependencies identified from the source. No root `requirements.txt` is currently listed.
5. Follow the code's run instructions; no verified command is available from the root file listing.

The project description mentions preprocessing, stratified splitting, Logistic Regression, and accuracy/precision/recall/F1 evaluation. This README does not claim that a particular result has been reproduced. Fit preprocessing only on training data, compare against a baseline, and consider class imbalance and the costs of false negatives.

## Privacy and testing

Use only appropriately licensed data and do not add real customer records. No root test command is currently documented. Tests should cover input validation, missing values, leakage prevention, and stable prediction output.


## Reproducible run

The training script is the extensionless root file `coustmer churn 11`; run it from the repository root so it can find `WA_Fn-UseC_-Telco-Customer-Churn.csv`.

```bash
python -m venv .venv
# Activate the environment, then:
python -m pip install --upgrade pip
pip install -r requirements.txt
python "coustmer churn 11"
```

The script writes threshold and model-comparison CSV files in the working directory. Review its validation/test selection logic before treating reported test metrics as an unbiased final estimate; model selection should be completed using validation data only, with the test set held back until the final chosen model.
