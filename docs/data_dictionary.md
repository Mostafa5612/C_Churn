Bank Customer Churn — Data Dictionary
Dataset Overview
The dataset contains 10,000 customer records and 12 columns covering demographic information, financial profiles, account activity, and churn labels.

Column Breakdown

customer_id (int64): Unique identifier for each customer (10,000 distinct values). Used purely for tracking and excluded from feature inputs.

credit_score (int64): Credit score recorded for the customer (460 distinct values). Input feature.

country (object): Customer's country of residence (3 distinct values). Input feature.

gender (object): Customer's gender (2 distinct values). Input feature.

age (int64): Customer's age in years (70 distinct values). Input feature.

tenure (int64): Years the customer has stayed with the bank (11 distinct values). Input feature.

balance (float64): Account balance measured before prediction (6,382 distinct values). Input feature.

products_number (int64): Number of bank products used by the customer (4 distinct values). Input feature.

credit_card (int64): Binary flag showing whether the customer owns a credit card (2 distinct values). Input feature.

active_member (int64): Binary flag showing if the customer is actively using bank services (2 distinct values). Input feature.

estimated_salary (float64): Estimated salary of the customer (9,999 distinct values). Input feature.

churn (int64): Target label indicating whether the customer left the bank (2 distinct values). Target variable only.

Data Types Summary

Integers (8 columns): customer_id, credit_score, age, tenure, products_number, credit_card, active_member, churn

Floats (2 columns): balance, estimated_salary

Objects / Strings (2 columns): country, gender