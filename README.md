💳 Credit Card Transactions & Fraud Analytics (SQL Case Study)

📖 Overview

This project is a SQL-based analytics case study focused on understanding credit card usage, customer behavior, credit limits, and fraud patterns for a leading bank.

The analysis simulates a real-world scenario handled by an Analytics & Risk Team, where transactional data is used to strengthen fraud detection systems and improve customer risk profiling.

🏦 Business Context

A bank issues multiple types of credit cards (Silver, Gold, Platinum, etc.) to customers across different segments. Customers perform thousands of transactions monthly through various channels such as Online, POS, and ATM.

Some transactions are later flagged as fraudulent, and the bank wants to analyze:

Spending behavior

Credit utilization

Fraud concentration

Card family performance

🎯 Objectives

Using SQL, this project answers business-driven questions such as:

Who are the high-spend customers?

Which card families have the highest and lowest credit limits?

Which customers or segments are more prone to fraud?

Which months experience higher fraud activity?

Which card types perform best with minimal fraud?

🗂️ Dataset Description
1. Card_base

Stores information about credit cards issued to customers.

Column Name	Description
Card_Number	Unique credit card number
Card_Family	Silver, Gold, Platinum, etc.
Credit_Limit	Credit limit assigned
Cust_ID	Customer identifier
2. Customer_base

Contains customer demographic and segmentation details.

Column Name	Description
Cust_ID	Unique customer ID
Age	Customer age
Customer_Segment	Mass / Affluent / HNI
Customer_Vintage_Group	<1 yr, 1–3 yrs, 3+ yrs
3. Transaction_base

Captures all credit card transactions.

Column Name	Description
Transaction_ID	Unique transaction ID
Transaction_Date	Date of transaction
Credit_Card_ID	Card used
Transaction_Value	Transaction amount
Transaction_Segment	Online / POS / ATM
4. Fraud_base

Indicates fraudulent transactions.

Column Name	Description
Transaction_ID	Linked transaction
Fraud_Flag	1 = Fraud, 0 = Not Fraud
🔗 Table Relationships
Customer_base.Cust_ID
        ↓
Card_base.Cust_ID
        ↓
Transaction_base.Credit_Card_ID
        ↓
Fraud_base.Transaction_ID

📊 Key Analysis Areas

✔ High-spender identification
✔ Credit limit analysis by card family
✔ Fraud rate by customer segment
✔ Monthly fraud trends
✔ Card performance without fraud

🧠 SQL Concepts Used

INNER JOIN / LEFT JOIN

GROUP BY & HAVING

CASE WHEN logic

Date functions (MONTH, YEAR)

Aggregations (SUM, COUNT, AVG)

Fraud rate calculations

📌 Example Business Questions

Which customers spend more than their peer average?

Which card family has the highest fraud percentage?

Do newer customers show higher fraud risk?

Are online transactions more fraud-prone?

Which card family has zero fraud exposure?

🛠️ Tools & Technologies

SQL (MySQL / PostgreSQL / SQL Server compatible)

Relational Data Modeling

Fraud Analytics

Risk & Customer Segmentation Analysis

🚀 Outcomes & Insights

This analysis enables the bank to:

Detect high-risk customer segments

Optimize credit limits

Strengthen fraud monitoring strategies

Improve card portfolio performance

📁 Repository Structure (Suggested)
📦 credit-card-fraud-analytics
 ┣ 📂 sql_queries
 ┃ ┣ high_spend_customers.sql
 ┃ ┣ fraud_analysis.sql
 ┃ ┣ card_family_performance.sql
 ┃ ┗ monthly_fraud_trends.sql
 ┣ 📄 README.md

👤 Author

Rohit Kumawat
SQL | Data Analytics | Risk & Fraud Analysis

⭐ Why This Project Matters

This case study reflects real banking analytics problems frequently asked in:

SQL interviews

Risk & fraud analytics roles

Data analyst assessments

Banking & fintech case rounds
