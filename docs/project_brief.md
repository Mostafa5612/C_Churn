1. Business Context
Customer churn occurs when clients close their accounts or stop using a bank's services. Because acquiring new customers is significantly more expensive than keeping existing ones, reducing churn is a top priority. This project uses a public bank dataset to examine customer characteristics and highlight patterns associated with churn. By combining exploratory data analysis, interactive Power BI reporting, and machine learning, the goal is to convert raw customer data into actionable retention strategies.

2. Target Audience

Bank Management: To get a clear view of customer loss trends and support long-term retention planning.

Customer Retention Teams: To identify specific customer segments that need direct outreach or tailored offers.

Data & Analytics Teams: To inspect churn indicators and evaluate predictive modeling techniques.

3. Project Objectives

Calculate the overall customer churn rate across the business.

Spot customer groups with disproportionately high churn rates.

Analyze how demographic and financial features relate to customer departures.

Build an interactive Power BI dashboard to share findings across teams.

Train and evaluate a classification model to flag high-risk customers.

Help retention teams prioritize which customer segments to focus on first.

4. Defining Churn
In this project, a churned customer is defined strictly by the dataset's target column (indicated as having left the bank). Because the dataset represents a snapshot without explicit observation windows or timestamps, we will not assume a specific time frame (such as 30 or 90 days). The target variable will be validated against raw data before running any analysis.

5. Core Business Questions

Overall Churn: What percentage of total customers have left the bank?

Geography: Which countries or regions experience the highest churn rates?

Demographics: How does churn rate vary across different age brackets?

Engagement: Are active members noticeably less likely to churn than inactive members?

Financial Profile: How do account balance and the number of products held impact churn?

Note: Group sizes will be reviewed during analysis to ensure small sample sizes do not skew conclusions.

6. Success Criteria

Power BI Dashboard

Displays core high-level metrics clearly (Total Customers, Churned Count, Churn Rate).

Offers interactive filters to slice data by demographics, location, and account details.

Presents clean, non-technical visuals that non-analysts can easily interpret.

Produces summary numbers that match the Python analysis exactly.

Machine Learning Model

Tested on an untouched holdout set.

Evaluated using Recall, Precision, F1-score, PR-AUC, and a Confusion Matrix.

Outperforms a standard baseline model while managing the trade-off between false alarms and missed churners (accuracy alone will not be used to judge performance).

7. Scope & Limitations
This analysis relies on a static public dataset rather than live banking systems. Because there is no temporal tracking, the project focuses on identifying patterns within the available snapshot rather than predicting future churn over a specific calendar period. Results highlight correlation rather than direct cause-and-effect, providing a solid foundation for further investigation by retention teams.

## Initial Dataset Findings

The dataset contains 10,000 customer records. Of these, 2,037 customers (20.37%) are labeled as churned, while 7,963 customers (79.63%) are labeled as not churned.

These figures represent the distribution of the churn target in the available dataset. The observation window and exact business definition of churn have not yet been confirmed.