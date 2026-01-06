## 💳 Credit Card Transactions & Fraud Analytics

###  🔹 Business Context

A leading bank issues multiple types of credit cards to its customers. These customers perform thousands of transactions every month across different merchant categories and channels. The bank also tracks which transactions are later identified as fraudulent so that it can strengthen its fraud detection systems and customer risk models.

#### As part of the bank’s Analytics & Risk team, you are given a dataset that captures:
  - The list of credit cards issued to customers and their credit limit.<br>
  - Core customer attributes such as age and customer segment.<br>
  - All card transactions performed over a certain period.<br>
  - Which transactions were flagged as fraudulent.

#### Your job is to explore this data using SQL and answer key business questions related to:

  - High-spend customers.<br>
  - Credit limit analysis.<br>
  - Fraud patterns and risk.<br>
  - Customer segments and behavior.<br>
  - Card family performance and usage.

### Available Tables
The dataset consists of four core tables.

#### 1. Card_base

| COLUMN_NAME  | DATA_TYPE        |
|--------------|------------------|
| Card_Number  | varchar(50)      |
| Card_Family  | varchar(30)      | -- e.g. Silver, Gold, Platinum
| Credit_Limit | int              |
| Cust_ID      | varchar(20)      |


#### 2. Customer_base


| COLUMN_NAME            | DATA_TYPE        |
|------------------------|------------------|
| Cust_ID                | varchar(20)      |
| Age                    | int              |
| Customer_Segment       | varchar(30)      | -- e.g. Mass, Affluent, HNI
| Customer_Vintage_Group | varchar(20)      | -- e.g. <1 yr, 1-3 yrs, 3| yrs



#### 3. Fraud_base


| COLUMN_NAME    | DATA_TYPE        |
|----------------|------------------|
| Transaction_ID | varchar(20)      |
| Fraud_Flag     | int              | -- 1 = fraud, 0 = not fraud (if present)



#### 4. Transaction_base


| COLUMN_NAME        | DATA_TYPE        |
|--------------------|------------------|
| Transaction_ID     | varchar(20)      |
| Transaction_Date   | date             |
| Credit_Card_ID     | varchar(50)      | -- links to Card_Number
| Transaction_Value  | decimal          |
| Transaction_Segment| varchar(20)      | -- e.g. Online, POS, ATM



### Typical relationships between the tables:

  --> Card_base.Cust_ID → Customer_base.Cust_ID.<br>
   --> Transaction_base.Credit_Card_ID → Card_base.Card_Number.<br>
   --> Fraud_base.Transaction_ID → Transaction_base.Transaction_ID.


### Case Study Objectives
Using these four tables, you will answer business-driven questions such as:

  --> How many customers are high spenders?<br>
  --> Which card families get the highest and lowest credit limits?<br>
  --> Which customers or segments are most associated with fraud?<br>
  --> Which month sees the highest fraud activity?<br>
  --> Which card types perform best without any fraud involvement?

### What You Will Learn
  --> Joining customer, card, transaction, and fraud tables.<br>
  --> Aggregating transactions at customer and card-family level.<br>
  --> Analyzing fraud patterns and risk.<br>
  --> Using date functions, grouping, and conditional logic.<br>
  --> Translating business questions into efficient SQL queries.

Use SQL to help the bank understand its customers, control fraud risk, and make smarter credit decisions.
