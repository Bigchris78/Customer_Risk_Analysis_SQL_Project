# SQL Customer Risk Analysis Project

## Project Overview

This project demonstrates how SQL can be used to analyze customer risk data in a simulated banking environment. The analysis combines customer information, risk scores, and transaction data to identify high-risk customers, summarize transaction activity, and support risk monitoring.

The project demonstrates SQL skills commonly used by Fraud Analysts, AML/KYC Analysts, Risk Analysts, Compliance Analysts, and Operations Analysts.

---

## Business Problem

Financial institutions assign risk ratings to customers based on various factors. Analysts must combine customer, risk, and transaction data to identify high-risk customers, monitor financial activity, and support fraud prevention and compliance efforts.

This project uses SQL to join multiple datasets and answer business questions related to customer risk.

---

## Project Objectives

- Combine customer and risk data using SQL JOINs
- Identify high-risk customers
- Analyze transaction activity by risk level
- Practice SQL skills used in analyst roles
- Produce business reports from multiple datasets

---

## Tools Used

- SQL
- DB Fiddle (or SQLite Online)
- Microsoft Excel (for creating sample datasets)

---

## Datasets

### Customers

| Column | Description |
|---------|-------------|
| customer_id | Unique customer identifier |
| customer_name | Customer's full name |
| state | Customer's state |

### Risk Scores

| Column | Description |
|---------|-------------|
| customer_id | Unique customer identifier |
| risk_score | Customer risk level (Low, Medium, High) |

### Transactions

| Column | Description |
|---------|-------------|
| transaction_id | Unique transaction identifier |
| customer_id | Customer who made the transaction |
| amount | Transaction amount in USD |

---

## Business Questions

This project answers the following questions:

1. Show every customer and their risk score.
2. Show only High-Risk customers.
3. Count customers in each risk category.
4. Calculate the total transaction amount for High-Risk customers.
5. Calculate the average transaction amount by risk level.
6. Identify which state has the most High-Risk customers.
7. Identify the highest-spending High-Risk customers.

---

## SQL Skills Demonstrated

- SELECT
- WHERE
- INNER JOIN
- GROUP BY
- ORDER BY
- COUNT
- SUM
- AVG

---

## Project Files

```text
sql-customer-risk-analysis/
│
├── README.md
├── customer_risk_analysis.sql
├── customers.csv
├── risk_scores.csv
├── transactions.csv
└── images/
```

---

## Sample Analysis

### Example Question

**How much money did High-Risk customers spend?**

The query joins the **transactions** and **risk_scores** tables, filters for customers with a **High** risk rating, and calculates the total amount they spent.

```sql
SELECT SUM(t.amount) AS high_risk_total
FROM transactions t
JOIN risk_scores r
ON t.customer_id = r.customer_id
WHERE r.risk_score = 'High';
```

### Example Question

**Which state has the most High-Risk customers?**

The query joins the customer and risk tables, filters for High-Risk customers, groups the results by state, and counts the number of customers in each state.

---

## Skills Developed

- SQL Query Writing
- Data Analysis
- Relational Database Concepts
- Data Aggregation
- Business Reporting
- Customer Risk Analysis
- Financial Data Analysis

---

## Future Improvements

Future enhancements may include:

- Fraud detection rules
- Suspicious transaction alerts
- Monthly transaction trend analysis
- Interactive Power BI dashboard
- Additional customer demographics

---

## Related Projects

- Fraud Transaction Monitoring Dashboard (Excel)
- Customer Risk Score Lookup (Excel)
- SQL Transaction Analysis

---

## Author

Christopher Walden

Aspiring Fraud Analyst | Risk Analyst | Compliance Analyst | Operations Analyst# Customer_Risk_Analysis_SQL_Project
