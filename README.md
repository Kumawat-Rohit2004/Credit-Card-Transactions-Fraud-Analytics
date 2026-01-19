## 💳 Credit Card Transactions & Fraud Analytics

### 📌 Project Overview
This project focuses on identifying fraudulent patterns and abnormal customer behaviors within credit card transaction data. By leveraging advanced SQL techniques and multi-table relational database structures, I performed an end-to-end analysis to detect high-risk transactions, analyze credit utilization, and provide data-driven insights for financial risk assessment.

### 🎯 Key Objectives
Fraud Detection: Analyze historical transaction data to identify patterns indicative of fraudulent activity.<br>
Behavioral Analysis: Segment customers based on spending habits and credit limit utilization to assess risk.<br>
Performance Insights: Evaluate how fraud is distributed across different card families and customer demographics.<br>
Business Impact: Provide actionable findings to reduce financial losses and improve the accuracy of credit decisions.

### 🛠️ Technical Stack
Database: PostgreSQL / MySQL <br>
Language: SQL (Complex Joins, CTEs, Window Functions, Aggregate Functions) <br>
Concepts: Data Normalization, Schema Design, Fraud Modeling, Risk Assessment.

### 📂 Database Schema & Analysis
The project built a relational structure by joining four primary datasets:

#### 1.Customer: Demographics and account details.
| COLUMN_NAME            | DATA_TYPE        |
|------------------------|------------------|
| Cust_ID                | varchar(20)      |
| Age                    | int              |
| Customer_Segment       | varchar(30)      | -- e.g. Mass, Affluent, HNI
| Customer_Vintage_Group | varchar(20)      | -- e.g. <1 yr, 1-3 yrs, 3| yrs

#### 2.Card: Information on card types and families.
| COLUMN_NAME  | DATA_TYPE        |
|--------------|------------------|
| Card_Number  | varchar(50)      |
| Card_Family  | varchar(30)      | -- e.g. Silver, Gold, Platinum
| Credit_Limit | int              |
| Cust_ID      | varchar(20)      |

#### 3.Transaction: Real-time spending data (amount, time, location).
| COLUMN_NAME        | DATA_TYPE        |
|--------------------|------------------|
| Transaction_ID     | varchar(20)      |
| Transaction_Date   | date             |
| Credit_Card_ID     | varchar(50)      | -- links to Card_Number
| Transaction_Value  | decimal          |
| Transaction_Segment| varchar(20)      | -- e.g. Online, POS, ATM

#### 4.Fraud: Flagged fraudulent instances.
| COLUMN_NAME    | DATA_TYPE        |
|----------------|------------------|
| Transaction_ID | varchar(20)      |
| Fraud_Flag     | int              | -- 1 = fraud, 0 = not fraud (if present)

### 🚀 Analysis Workflow
Data Integration: Executed multi-table SQL joins across customer and transaction datasets to enable comprehensive analysis.<br>
Risk Assessment: Analyzed credit limit utilization ratios to identify customers at high risk of default or suspicious activity.<br>
Trend Identification: Evaluated the frequency and volume of fraud across various customer segments.<br>
Actionable Insights: Correlated spending spikes with fraud flags to help institutions refine their detection algorithms.

### 📊 Key Findings
Identified specific "Card Families" that experienced higher fraud distribution.<br>
Highlighted segments where high credit limit utilization strongly correlated with abnormal behavior.<br>
Provided data-backed recommendations to reduce financial losses through targeted fraud monitoring.










