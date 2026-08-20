# Customer Shopping Behavior Analysis

Analysis of 3,900 customer transactions to uncover spending patterns, customer segments, product preferences, and subscription behavior — supporting data-driven business decisions.

## Overview

- **Rows:** 3,900 transactions
- **Columns:** 18 (demographics, purchase details, shopping behavior)
- **Tools used:** Python (pandas), PostgreSQL, Power BI

## Workflow

1. **Data Cleaning (Python)**
   - Loaded and explored data with `pandas` (`df.info()`, `.describe()`)
   - Imputed 37 missing `Review Rating` values using category-wise medians
   - Standardized column names to snake_case
   - Engineered `age_group` and `purchase_frequency_days` features
   - Checked redundancy between `discount_applied` and `promo_code_used`; dropped the latter
   - Loaded cleaned data into PostgreSQL

2. **Business Analysis (SQL)**
   - Revenue by gender
   - High-spending discount users
   - Top 5 products by rating
   - Shipping type comparison (Standard vs. Express)
   - Subscribers vs. non-subscribers spend/revenue
   - Discount-dependent products
   - Customer segmentation (New / Returning / Loyal)
   - Top 3 products per category
   - Repeat buyers vs. subscription likelihood
   - Revenue by age group

3. **Visualization (Power BI)**
   - Interactive dashboard with filters for subscription status, gender, category, and shipping type
   - KPIs: customer count, average purchase amount, average review rating
   - Charts: revenue/sales by category and age group, subscription split

## Key Findings

- Male customers generated significantly more revenue ($157,890) than female customers ($75,191)
- Loyal customers make up the majority of the base (3,116 of 3,900)
- Only 27% of customers are subscribers, yet non-subscribers drive most total revenue
- Hats, Sneakers, and Coats are the most discount-dependent products
- Young Adults contribute the highest revenue by age group

## Recommendations

- Boost subscriptions with exclusive member benefits
- Launch loyalty programs to convert Returning customers into Loyal ones
- Review discount policy to balance sales growth with margins
- Highlight top-rated, best-selling products in marketing campaigns
- Target high-revenue age groups and express-shipping users

## Project Structure

```
├── data/              # Raw and cleaned datasets
├── notebooks/         # Python EDA and cleaning scripts
├── sql/               # SQL queries for business analysis
├── dashboard/         # Power BI (.pbix) file
└── README.md
```
