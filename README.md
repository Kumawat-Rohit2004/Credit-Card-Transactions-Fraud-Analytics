Credit Card Transactions & Fraud Analytics (SQL Case Study)
📌 Business Context

A leading bank issues multiple types of credit cards to its customers. These customers perform thousands of transactions every month across various merchant categories and channels. Some of these transactions are later identified as fraudulent.

To strengthen fraud detection systems and improve customer risk models, the bank maintains detailed data on customers, credit cards, transactions, and fraud flags.

As part of the Analytics & Risk Team, this project focuses on exploring and analyzing this data using SQL to derive meaningful business insights.

🎯 Project Objectives

Using SQL, this case study aims to answer key business-driven questions related to:

High-spend customers and spending behavior

Credit limit distribution across card families

Fraud patterns and customer risk profiling

Transaction trends over time

Card family performance with respect to fraud

📂 Dataset Overview

The dataset consists of four core tables representing customers, cards, transactions, and fraud details.

1️⃣ Card_base

Contains information about credit cards issued to customers.

Column Name	Data Type	Description
Card_Number	varchar(50)	Unique card identifier
Card_Family	varchar(30)	Card type (Silver, Gold, Platinum, etc.)
Credit_Limit	int	Credit limit assigned to the card
Cust_ID	varchar(20)	Linked customer ID
2️⃣ Customer_base

Stores demographic and segmentation details of customers.

Column Name	Data Type	Description
Cust_ID	varchar(20)	Unique customer identifier
Age	int	Customer age
Customer_Segment	varchar(30)	Mass, Affluent, HNI
Customer_Vintage_Group	varchar(20)	<1 yr, 1–3 yrs, 3+ yrs
3️⃣ Transaction_base

Captures all credit card transactions.

Column Name	Data Type	Description
Transaction_ID	varchar(20)	Unique transaction identifier
Transaction_Date	date	Date of transaction
Credit_Card_ID	varchar(50)	Card used for transaction
Transaction_Value	decimal	Transaction amount
Transaction_Segment	varchar(20)	Online, POS, ATM
4️⃣ Fraud_base

Indicates whether a transaction was fraudulent.

Column Name	Data Type	Description
Transaction_ID	varchar(20)	Linked transaction ID
Fraud_Flag	int	1 = Fraud, 0 = Not Fraud
🔗 Table Relationships

Card_base.Cust_ID → Customer_base.Cust_ID

Transaction_base.Credit_Card_ID → Card_base.Card_Number

Fraud_base.Transaction_ID → Transaction_base.Transaction_ID

📊 Business Questions Addressed

This case study answers questions such as:

How many customers qualify as high spenders?

Which card families have the highest and lowest credit limits?

Which customer segments are most prone to fraud?

Which month experiences the highest fraud activity?

Which card families perform best with minimal or no fraud?

🛠️ Skills & Concepts Used

SQL joins across multiple tables

Aggregation and grouping

Fraud analysis using conditional logic

Date-based trend analysis

Customer and card-level behavioral insights

🚀 Outcome

By translating business questions into efficient SQL queries, this project helps the bank:

Understand customer spending behavior

Identify fraud-prone segments

Improve risk control strategies

Make smarter credit and card portfolio decisions

✅ Ideal for: SQL practice, analytics interviews, risk & fraud case studies, and portfolio projects.
