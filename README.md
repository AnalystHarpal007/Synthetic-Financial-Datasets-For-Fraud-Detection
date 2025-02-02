# Synthetic-Financial-Datasets-For-Fraud-Detection

**Project Overview**
This project focuses on detecting fraudulent transactions in a large banking dataset using advanced SQL queries. The dataset, sourced from Kaggle, contains transaction details such as origin and destination accounts, transaction amounts, balances, and fraud indicators. We use SQL techniques like recursive CTEs, window functions, subqueries, and complex joins to identify suspicious activity and validate transaction consistency.

Dataset
Source: Kaggle - Paysim1 Banking Dataset
File: PS_20174392719_1491204439457_log.csv
Columns:
step: Time step of the transaction.
type: Type of transaction (TRANSFER, CASH_OUT, etc.).
amount: Transaction amount.
nameOrig: Origin account identifier.
oldbalanceOrg: Initial balance of the origin account.
newbalanceOrig: Updated balance of the origin account.
nameDest: Destination account identifier.
oldbalanceDest: Initial balance of the destination account.
newbalanceDest: Updated balance of the destination account.
isFraud: Indicates if the transaction is fraudulent.
isFlaggedFraud: Indicates if the transaction was flagged as potentially fraudulent.
SQL Queries Overview
Recursive Fraudulent Transaction Detection:

Detects chains of fraudulent transfers across accounts.
Rolling Fraud Detection:

Tracks fraudulent behavior within a 5-step window using SQL window functions.
Complex Fraud Detection with Multiple CTEs:

Identifies accounts with suspicious activity based on large transfers, no balance changes, and flagged transactions.
Balance Validation:

Validates whether computed balances match the actual balances in the dataset.
