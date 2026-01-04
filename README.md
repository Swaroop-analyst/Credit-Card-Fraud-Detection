💳 Credit Card Fraud Detection

End-to-End Machine Learning Project | Finance Analytics | CRISP-DM Framework

📌 Business Understanding

Credit card fraud causes significant financial losses for banks and payment processors.
This project builds a robust machine learning system to detect fraudulent transactions in real-time, improve customer protection, and reduce financial risk.

Business Goals

Maximize fraud detection rate

Minimize false alarms

Reduce monetary loss from fraudulent transactions

📊 Data Understanding

Dataset: Kaggle Credit Card Transactions
Records: ~1.3M transactions
Target Variable: is_fraud (0 = legitimate, 1 = fraud)

Class Distribution

Key Observations

Highly imbalanced dataset (fraud < 1%)

Fraud transactions tend to have higher amounts

Certain merchant categories & hours show elevated fraud risk

Large geographic distance between customer & merchant correlates with fraud

🧹 Data Preparation
Feature Engineering

Time features: hour, day, month

Geographic distance between customer & merchant

Categorical encoding

Standardization

SMOTE applied for class imbalance handling

Leakage Prevention

Removed identifiers & non-predictive fields:
cc_num, trans_num, names, addresses, DOB, timestamps

🤖 Modeling

Models trained:

Logistic Regression (baseline)

Light GBM

Random Forest

XGBoost (final production model)

 Model Evaluation Metric: ROC-AUC

 <img width="734" height="238" alt="image" src="https://github.com/user-attachments/assets/3238d2c6-2fe5-4ffe-a1fb-677b1c4e3305" />

Interpretation

97% of all fraudulent transactions are successfully detected by the final model.

High recall ensures minimal financial leakage from missed fraud.

Precision is intentionally lower — in fraud detection, false positives are far less costly than false negatives.

LightGBM was selected as the production model due to its strong performance and faster training speed.

🧠 Model Explainability (SHAP)
Feature Impact on Fraud Prediction

This ensures model transparency, regulatory compliance, and stakeholder trust.

💰 Business Impact Simulation

Estimated fraud savings:

On the validation dataset:

Total fraud cases: 647

Fraud detected by LightGBM: ~628 transactions (97%)

Assuming an average fraud loss of ₹5,000 per transaction:

Estimated prevented fraud loss ≈ ₹3.14 million
(on the validation sample alone)

This model demonstrates strong potential to significantly reduce financial losses and improve risk management.

When extrapolated to full production scale, this system has the potential to prevent multi-crore annual financial losses, significantly strengthening the organization’s risk management framework.

**Strategic Business Benefits**

Early fraud interception reduces direct monetary losses.

High-recall system protects customer trust and regulatory standing.

Explainable ML (SHAP) ensures auditability and compliance with financial governance standards.

Enables dynamic threshold tuning to balance operational cost vs fraud risk.

🚀 Deployment Readiness

This project delivers a production-ready fraud detection system capable of capturing 97% of fraudulent activity, translating machine learning performance directly into measurable financial value and operational risk reduction.

Preprocessing pipeline saved

Trained model serialized

Real-time inference supported

Monitoring & threshold tuning enabled

🧱 Tech Stack

Python | Pandas | Scikit-Learn | XGBoost | SHAP | Matplotlib | Seaborn | Imbalanced-Learn

📂 Repository Structure
credit-card-fraud-detection/
│
├── data/
├── notebooks/
├── models/
└── README.md
