# Intermediate SQL - Sales Analysis

## Overview
This project explores customer behavior and revenue patterns using SQL on the **Contoso dataset** (Microsoft sample data).
The analysis is built on a cohort-based view [cohort_analysis](cohort_analysis_view.sql) that aggregates sales by customer, including lifetime value, order history, and cohort year.
The goal is to answer key business questions around customer segmentation, cohorts, and retention to support data-driven decision-making. This analysis is part of the SQL+ course provided by **Luke Barousse**.

## Business Questions

1. **Customer Segmentation:** Who are our most valuable customers?<br>
2. **Cohort Analysis:** How do different customer groups generate revenue? <br>
3. **Retention Analysis:** Who hasn't purchased recently?

## Analysis Approach

### 1. Customer Segmentation

🖥️ Query: [1_customer_segmentation.sql](1_customer_segmentation.sql)

**📈 Visualization:**

![Customer_segmentation.png](/Dashboards/images/1_customer_segmentation.png)

📊 **Key Findings:**
- Customers were segmented into Low-, Mid-, and High-Value groups using LTV quartiles.
- The High-Value Segment (top 25%) contributes a disproportionately large share of total revenue.
- The Low-Value Segment is the largest by customer count but contributes the least revenue.

💡 **Business Insights**
- High-Value customers should be prioritized through account management, loyalty programs, and exclusive offers.
- Mid-Value customers are promising candidates for upsell/cross-sell campaigns → potential to grow into High-Value.
- Low-Value customers are less profitable; mass, low-cost marketing may be the most efficient way to engage them.

### 2. Cohort Analysis

🖥️ Query: [2_cohort_analysis.sql](2_cohort_analysis.sql)

**📈 Visualization:**

![2_cohort_analysis.png](/Dashboards/images/2_cohort_analysis.png)

📊 **Key Findings:**
- Each cohort year shows different average revenue per customer.
- Earlier cohorts (older customers) tend to have higher total revenue, reflecting longer relationships.
- Newer cohorts have lower revenue per customer, suggesting onboarding and growth opportunities.

💡 **Business Insights**
- Cohorts confirm that customer value grows over time if retention is maintained.
- Accelerating revenue growth in new cohorts requires strong onboarding campaigns.
- Comparing cohorts helps assess whether recent marketing campaigns are attracting more valuable customers.

### 3. Retention Analysis

🖥️ Query: [3_customer_retention.sql](3_customer_retention.sql)

**📈 Visualization:**

![3_customer_retention.png](/Dashboards/images/3_customer_retention.png)

📊 **Key Findings:**
- A significant portion of customers are inactive or churned (>6 months since last purchase).
- Retention rates vary by cohort year — some years retain a stronger customer base than others.
- Recent cohorts show higher churn, possibly due to lack of engagement or ineffective onboarding.


💡 **Business Insights**
- Retention is a weak point → opportunities exist for churn-prevention strategies (reminders, loyalty programs, targeted campaigns).
- Older cohorts demonstrate loyalty and should be nurtured through engagement and appreciation programs.
- Newer cohorts disengage faster → onboarding and early engagement strategies must be strengthened.

## Strategic Recommendations

1. Invest in loyalty programs targeting High-Value customers to secure long-term engagement.
2. Personalized onboarding campaigns for new cohorts to increase their average revenue.
3. Reactivation campaigns (discounts, emails, outreach) for churned customers.
4. Cohort tracking dashboard in BI tools (Power BI, Tableau) to monitor retention trends in real-time.

## Technical Details
- **Database:** PostgreSQL
- **Analysis Tools:** PostgreSQL, DBeaver, VS Code
- **Visualization:** ChatGPT

## Dataset
- **Source:** Microsoft Contoso sample dataset
- **Scope:** Sales, customers, stores, date and exchangerate
- **Note:** Data is for educational purposes only, not actual company data
