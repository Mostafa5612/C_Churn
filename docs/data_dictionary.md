# Bank Customer Churn — Data Dictionary

## Dataset Overview

The dataset contains 10,000 customer records and 12 columns covering demographic information, financial profiles, account activity, and churn labels.

The dataset is a static snapshot without confirmed observation dates or an explicit prediction window. Feature availability at prediction time must be verified before building a predictive model.

## Column Breakdown

**customer_id (int64):** Unique identifier for each customer (10,000 distinct values, ranging from 15,565,701 to 15,815,690). Used purely for tracking and excluded from feature inputs.

**credit_score (int64):** Credit score recorded for the customer (460 distinct values, ranging from 350 to 850). Input feature; availability at prediction time requires confirmation.

**country (object):** Customer's country of residence (3 distinct values: France, Germany, Spain). Input feature; availability at prediction time requires confirmation.

**gender (object):** Customer's gender (2 distinct values: Female, Male). Input feature; availability at prediction time requires confirmation.

**age (int64):** Customer's age in years (70 distinct values, ranging from 18 to 92). Input feature; availability at prediction time requires confirmation.

**tenure (int64):** Years the customer has stayed with the bank (11 distinct values, ranging from 0 to 10). Input feature; availability at prediction time requires confirmation.

**balance (float64):** Account balance (6,382 distinct values, ranging from 0 to 250,898.09). Input feature; timing of availability before prediction requires confirmation.

**products_number (int64):** Number of bank products used by the customer (4 distinct values, ranging from 1 to 4). Input feature; availability at prediction time requires confirmation.

**credit_card (int64):** Binary flag showing whether the customer owns a credit card (2 distinct values: 0 = No, 1 = Yes). Input feature; availability at prediction time requires confirmation.

**active_member (int64):** Binary flag showing if the customer is actively using bank services (2 distinct values: 0 = No, 1 = Yes). Input feature; timing and definition of activity require confirmation.

**estimated_salary (float64):** Estimated salary of the customer (9,999 distinct values, ranging from 11.58 to 199,992.48). Input feature; availability at prediction time requires confirmation.

**churn (int64):** Target label indicating whether the customer left the bank (2 distinct values: 0 = Not churned, 1 = Churned). Target variable only; must never be used as an input feature.

## Data Types Summary

**Integers (8 columns):** customer_id, credit_score, age, tenure, products_number, credit_card, active_member, churn.

**Floats (2 columns):** balance, estimated_salary.

**Objects / Strings (2 columns):** country, gender.

## Data Quality and Leakage Notes

- `customer_id` is an identifier and must be excluded from model features.
- `churn is the target variable and must never be included as an input feature.
- Numeric ranges and allowed values are based on the current raw dataset and should be rechecked if the dataset changes.
- Feature availability and timing relative to churn must be confirmed before model training.
- The dataset does not provide a confirmed observation window, so no specific time period is assumed.