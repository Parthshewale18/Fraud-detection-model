### Fraud Detection in Financial Transactions
This project is focused on building a machine learning pipeline to proactively detect fraudulent financial transactions using a large-scale dataset (6.3M+ rows). The goal is to identify and understand fraudulent patterns, enhance detection accuracy, and propose actionable security measures for financial institutions.

📊 Dataset Overview
The dataset simulates 30 days of mobile money transactions. Key features include:

Transaction metadata such as type (PAYMENT, TRANSFER, etc.)

Account balances before and after each transaction

Fraud flags indicating confirmed and flagged fraudulent activity

📝 Source: Synthetic transaction data with over 6 million records and labeled fraud instances.

⚙️ Project Pipeline
1. Data Cleaning & Preprocessing
Handled missing and inconsistent balance data

Removed redundant or high-collinearity features

Engineered domain-driven features like deltaOrig, deltaDest, and isMerchantDest

2. Feature Engineering
Created balance difference indicators to capture inconsistencies

Encoded transaction types using One-Hot Encoding

Flagged whether the recipient was a merchant

3. Modeling
Used Random Forest as the primary classifier

Applied SMOTE to handle extreme class imbalance

Evaluated with metrics suited for imbalanced datasets: F1-Score, ROC-AUC, and PR-AUC


📈 Results
High recall and precision for fraudulent cases

Key predictors: 
deltaOrig         0.371269
oldbalanceOrg     0.139289
newbalanceOrig    0.136983
amount            0.068940

Strong model generalization with PR-AUC and ROC-AUC scores indicating effective separation

🛡 Recommendations
Based on insights, the following security measures are recommended:

Real-time flagging of high-value and inconsistent transactions

Multi-factor authentication for cash-out and transfer types

Transaction pattern monitoring and account freezing for flagged behavior

