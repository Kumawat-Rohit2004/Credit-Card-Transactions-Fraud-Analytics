💳 Credit Card Transactions & Fraud Analytics

A SQL-Driven Banking Analytics Case Study

📌 Overview

This project explores credit card transactions and fraud analytics for a leading bank using SQL.
The goal is to analyze customer behavior, credit limits, transaction trends, and fraud patterns to support risk management and smarter credit decisions.

This case study simulates the real-world responsibilities of an Analytics & Risk Team in the banking and fintech domain.

🏦 Business Context

A leading bank issues multiple types of credit cards to its customers. These customers perform thousands of transactions every month across different merchant categories and channels.

The bank also tracks transactions that are later identified as fraudulent, enabling it to:

Improve fraud detection systems

Reduce financial risk

Enhance customer trust

Strengthen risk-based decision-making

As part of the Analytics & Risk Team, you are provided with structured datasets covering customers, cards, transactions, and fraud indicators.

🎯 Project Objectives

Using SQL, this project answers key business questions such as:

🔹 Who are the high-spend customers?

🔹 How are credit limits distributed across card families?

🔹 Which customers or segments are more fraud-prone?

🔹 Which months see higher fraud activity?

🔹 Which card families perform best with minimal fraud?

🗂️ Dataset Description

The dataset consists of four core tables:

🪪 Card_base

Stores details of credit cards issued to customers.

Column Name	Data Type	Description
Card_Number	varchar(50)	Unique card identifier
Card_Family	varchar(30)	Silver, Gold, Platinum
Credit_Limit	int	Credit limit assigned
Cust_ID	varchar(20)	Customer ID
👤 Customer_base

Contains demographic and segmentation information.

Column Name	Data Type	Description
Cust_ID	varchar(20)	Unique customer identifier
Age	int	Customer age
Customer_Segment	varchar(30)	Mass / Affluent / HNI
Customer_Vintage_Group	varchar(20)	<1 yr, 1–3 yrs, 3+ yrs
💳 Transaction_base

Records all credit card transactions.

Column Name	Data Type	Description
Transaction_ID	varchar(20)	Unique transaction ID
Transaction_Date	date	Date of transaction
Credit_Card_ID	varchar(50)	Linked card number
Transaction_Value	decimal	Transaction amount
Transaction_Segment	varchar(20)	Online / POS / ATM
🚨 Fraud_base

Indicates fraudulent transactions.

Column Name	Data Type	Description
Transaction_ID	varchar(20)	Linked transaction
Fraud_Flag	int	1 = Fraud, 0 = Not Fraud
🔗 Table Relationships

Card_base.Cust_ID → Customer_base.Cust_ID

Transaction_base.Credit_Card_ID → Card_base.Card_Number

Fraud_base.Transaction_ID → Transaction_base.Transaction_ID

📊 Key Analysis Areas

✔ High-spender identification
✔ Credit limit comparison by card family
✔ Fraud analysis by customer segment
✔ Monthly fraud trend analysis
✔ Fraud-free card family performance

🧠 SQL Concepts Used

INNER JOIN & LEFT JOIN

GROUP BY & HAVING

CASE WHEN conditions

Date functions (MONTH, YEAR)

Aggregations (SUM, COUNT, AVG)

Fraud rate calculations
