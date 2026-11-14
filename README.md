# Customer Churn Prediction

> A binary-classification study that estimates which telecom customers are more likely to discontinue service.

## Project objective
Customer churn is a business problem: losing an existing customer can affect recurring revenue and increase acquisition costs. This project uses the Telco Customer Churn dataset to explore how customer account and service attributes relate to churn, then compares classification models and decision thresholds.

## Workflow
1. Load the Telco dataset from `WA_Fn-UseC_-Telco-Customer-Churn.csv`.
2. Normalize column names, convert blank values to missing values, and remove duplicate rows.
3. Convert `TotalCharges` to numeric and remove rows without a valid target or required charge value.
4. Encode the target `Churn` as a binary label: Yes = 1, No = 0.
5. Exclude the customer identifier from model inputs.
6. Create stratified training, validation, and test splits to preserve the class distribution.
7. One-hot encode categorical features and align validation/test columns with the training feature set.
8. Compare multiple classifiers, including Logistic Regression, Random Forest, Gradient Boosting, Decision Tree, SVM, Extra Trees, KNN, and AdaBoost.
9. Search decision thresholds on validation probabilities rather than assuming 0.50 is always optimal.
10. Evaluate the selected model on held-out test data.

## Why threshold tuning matters
A churn model is not only about accuracy. A business may prefer higher recall to identify more customers at risk, while still needing acceptable precision to avoid wasting retention resources. The script evaluates precision, recall, and F1 across candidate thresholds and uses a precision constraint when selecting a threshold.

## Metrics
The experiment includes Accuracy, Precision, Recall, F1-score, and ROC-AUC where available. No single metric describes every business use case; the appropriate operating threshold depends on the cost of false positives and false negatives.

## Run locally
Python 3.10+ is recommended.
```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS / Linux
source .venv/bin/activate
python -m pip install --upgrade pip
pip install pandas numpy scikit-learn
python "coustmer churn 11"
```
Run the command from the repository root because the script reads the CSV using a relative path.

## Repository contents
- `WA_Fn-UseC_-Telco-Customer-Churn.csv` — input dataset.
- `coustmer churn 11` — Python classification experiment.

## Responsible interpretation
Predicted churn is a probability or risk signal, not proof that a customer will leave. Use predictions to support fair, helpful retention analysis—not to deny service or make consequential decisions automatically. Dataset quality, class imbalance, threshold choice, and validation design all affect the result.

## Skills demonstrated
Binary classification · Customer analytics · Data cleaning · Categorical encoding · Stratified sampling · Threshold optimization · Model comparison · Classification metrics
