# E-Commerce Customer Intelligence, Churn Prediction & Revenue Optimization

An end-to-end **Data Analytics portfolio project** built using **Python, PostgreSQL/SQL, and Power BI** to analyze customer behavior, identify churn risk, understand revenue drivers, and generate actionable business recommendations.

---

## Project Overview

This project follows a complete analytics workflow:

**Data Quality & Cleaning → Customer Analytics → SQL Business Analysis → Churn Prediction → Power BI Dashboards → Business Recommendations**

The analysis focuses on five major business areas:

- Customer intelligence and segmentation
- Customer value and purchase behavior
- Product and category performance
- Churn-risk prediction and retention
- Revenue and discount optimization

---

## Business Objectives

1. Understand customer purchasing behavior.
2. Segment customers using RFM analysis.
3. Identify repeat, one-time, high-value, and at-risk customers.
4. Analyze product and category revenue performance.
5. Track monthly and yearly revenue trends.
6. Measure the impact of discounts on revenue.
7. Predict customers who are at risk of future inactivity.
8. Convert analytical findings into practical retention and revenue strategies.

---

## Dataset

A project-specific analytical dataset was prepared from the source data.

### Final Dataset Scale

| Metric | Value |
|---|---:|
| Cleaned Records | 89,913 |
| Unique Orders | 35,390 |
| Unique Customers | 16,544 |
| Unique Products | 550 |
| Categories | 22 |
| Date Range | 2023-01-02 to 2025-12-31 |

---

# Project Structure

```text
Ecommerce_Customer_Intelligence
│
├──.gitignore
│
├── 01_Raw_Data
│   ├── ecommerce_data_90000.csv
│   └── README.md
│
├── 02_Python
│   ├── scripts
│   └── outputs
│
├── 03_SQL
│   ├── ecommerce_customer_intelligence_analysis.sql
│   └── final_validation.sql
│
├── 04_PowerBI
│   ├── Executive Overview.pbix
│   ├── Customer Intelligence.pbix
│   ├── Dashboard_1_Executive_Overview.png
│   ├── Dashboard_2_Customer_Intelligence.png
│   ├── Dashboard_3_Churn_and_Risk.png
│   └── Dashboard_4_Revenue_Optimization.png
│
├── 05_Reports
│   └── Ecommerce_Customer_Intelligence_Complete_Project_Report.pdf
│
└──  README.md
```


# Python Analysis

Python was used for data preparation, customer analytics, time-series analysis, cohort analysis, discount analysis, and churn modeling.

### Python Workflow

- Data quality validation
- Duplicate detection and removal
- Date and numeric conversion
- Sales and revenue calculations
- RFM analysis
- RFM segmentation
- Segment validation
- Product and category analysis
- Monthly and yearly analysis
- Cohort retention analysis
- Customer behavior analysis
- Discount and revenue analysis
- Churn feature engineering
- Churn prediction
- Model evaluation
- Business interpretation

### RFM Segments

- Champions
- Loyal Customers
- Potential Loyalists
- At Risk
- Lost Customers
- Need Attention

---

# SQL / PostgreSQL Analysis

The cleaned dataset was analyzed using PostgreSQL.

### Database

- **Database:** `ecommerce_customer_intelligence`
- **Main Table:** `ecommerce_sales`

### SQL Topics

- SELECT
- WHERE
- GROUP BY
- HAVING
- Aggregate Functions
- CASE WHEN
- JOINs
- Subqueries
- CTEs
- Window Functions
- Ranking
- Date Functions
- String Functions
- Customer Segmentation
- Revenue Analysis
- Churn-Risk Analysis
- Data Validation

The SQL validation confirms:

- 89,913 records
- 35,390 orders
- 16,544 customers
- 550 products

---

# Churn Prediction

A **time-based churn-risk modeling approach** was used to reduce target leakage.

Historical customer behavior was used to predict whether a customer would become inactive during a defined future period.

### Model Performance

**ROC-AUC: approximately 0.84**

This indicates useful predictive separation between customers who were more likely and less likely to become inactive in the defined future window.

> The model should be interpreted as **future inactivity / churn-risk prediction**, not as a claim of ground-truth churn labels.

### Important Churn Drivers

The feature-impact analysis shows that:

- **Recency** is the strongest risk signal.
- Higher recent inactivity increases churn risk.
- Customer order behavior contributes significantly to risk.
- Revenue and item-level behavior also provide useful signals.

---

# Power BI Dashboards

The project contains four business-focused dashboard views.

## Dashboard 1 — Executive Overview

Provides a high-level view of:

- Net Revenue
- Orders
- Customers
- Average Order Value
- Repeat Customer Rate
- Revenue Trends
- Category Performance
- Top Products
- Top Cities
- Customer Segmentation

## Dashboard 2 — Customer Intelligence

Focuses on:

- RFM Segmentation
- Customer Revenue by Segment
- Repeat vs One-Time Customers
- Customer Value
- Top Customers
- Category Performance
- Customer Acquisition & Retention

## Dashboard 3 — Churn & Risk Intelligence

Focuses on:

- High-Risk Customers
- Revenue at Risk
- Churn Probability
- Risk Distribution
- Revenue by Risk Level
- Churn Feature Impact
- High-Risk Customer Priorities
- Retention Recommendations

## Dashboard 4 — Revenue Optimization

Focuses on:

- Gross vs Net Revenue
- Discount Impact
- Revenue by Discount Range
- Category Performance
- Category Discount Impact
- Annual Revenue Growth
- Top Products
- Revenue Optimization

---

# Key Business KPIs

| KPI | Result |
|---|---:|
| Total Customers | 16,544 |
| Total Orders | 35,390 |
| Total Items Sold | 207,069 |
| Gross Revenue | ₹988.89M |
| Total Discount | ₹128.09M |
| Net Revenue | ₹860.80M |
| Average Order Value | ₹24,323.28 |
| Repeat Customers | 9,218 |
| Repeat Customer Rate | 55.72% |
| Repeat Customer Revenue | ₹695.10M |
| Average Discount | 12.95% |

---

# Key Business Insights

### 1. Repeat Customers Drive Revenue

Repeat customers generated approximately **80.75% of total revenue**, showing that customer retention is a major revenue driver.

### 2. Electronics Is the Leading Category

Electronics generated approximately **₹430.29M in net revenue**, making it the strongest category in the analysis.

### 3. High-Value Customers Matter Disproportionately

The Very High Value customer group contributes the majority of revenue, making high-value customer retention a key business priority.

### 4. Revenue Increased Strongly in 2025

2025 generated approximately **₹400.69M in net revenue**, compared with approximately ₹227.03M in 2024.

### 5. Discounting Requires Optimization

The overall average discount is approximately **12.95%**. Higher discount ranges reduce realized revenue, so discounting should be targeted rather than applied broadly.

### 6. Churn Risk Creates a Retention Opportunity

The historical churn-risk model achieved approximately **0.84 ROC-AUC**, providing a practical framework for prioritizing customers for retention campaigns.

---

# Business Recommendations

### Customer Retention
- Prioritize high-risk and high-value customers.
- Create personalized retention campaigns.
- Use RFM segments to tailor offers.

### Revenue Optimization
- Monitor discount effectiveness by category and product.
- Avoid unnecessary deep discounts.
- Focus promotions on products/categories where discounts generate incremental value.

### Customer Value
- Build loyalty programs for repeat customers.
- Develop cross-sell and upsell campaigns.
- Protect Very High Value customers with personalized experiences.

### Churn Management
- Trigger retention campaigns for high-risk customers.
- Combine churn probability with customer revenue to prioritize the highest-value recovery opportunities.
- Monitor risk continuously as new transaction data becomes available.

---

# Tools & Technologies

### Programming
- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

### Database
- PostgreSQL
- SQL

### Business Intelligence
- Power BI
- DAX

### Development & Version Control
- VS Code
- Git
- GitHub

---

# Project Outcome

This project demonstrates an end-to-end Data Analyst workflow:

**Data Cleaning → Exploratory Analysis → Customer Segmentation → SQL Analytics → Churn Prediction → Power BI → Business Recommendations**

It combines technical analytics with business decision-making and is designed for portfolio presentation for:

- Data Analyst
- Business Analyst
- BI Analyst
- Customer Analytics
- Business Intelligence roles

---

# Author

**Masum Rabbani**

Aspiring Data Analyst | SQL | Python | Power BI | Business Intelligence

---

## Portfolio Highlights

**89K+ transaction records analyzed**  
**35K+ orders analyzed**  
**16K+ customers analyzed**  
**4 Power BI dashboards**  
**15+ Python analytical scripts**  
**Advanced SQL analysis with CTEs and Window Functions**  
**Churn-risk model with ~0.84 ROC-AUC**
