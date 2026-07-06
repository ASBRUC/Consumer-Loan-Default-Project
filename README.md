# Credit Risk Triage Model

## Goal
Build an interpretable model to predict bad-credit risk and create a triage policy that routes applicants to auto-approve, manual review, or auto-decline.

## Dataset
Statlog German Credit dataset with 1,000 applicant records. The target variable is `bad_credit`, where 1 indicates bad credit and 0 indicates good credit.

## Methods
- SQLite feature table and risk segmentation
- Exploratory analysis of bad rates by checking status and loan duration
- Logistic Regression baseline
- Random Forest benchmark
- Threshold-based triage policy using predicted probabilities

## Key Findings
- Checking status and loan duration showed meaningful separation in bad-credit rates.
- Logistic Regression achieved ROC-AUC around 0.81 and produced interpretable coefficients.
- Chosen thresholds created low-risk, manual-review, and high-risk buckets with clear differences in observed bad rate.

## Ethics and Limitations
Sensitive attributes were excluded from modeling. Results are based on a small historical dataset and should be validated further before real-world use.

## Next Steps
- Cross-validation stability check
- Probability calibration
- Fairness evaluation
- Cost-based threshold selection
