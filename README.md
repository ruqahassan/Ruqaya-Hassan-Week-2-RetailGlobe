# RetailGlobe Customer Segmentation using RFM Analysis and K-Means Clustering

## Overview

This repository contains a complete customer segmentation project developed for the RetailGlobe Ltd. marketing analytics capstone. The objective is to help the Marketing Director identify valuable customer groups and create targeted marketing strategies instead of treating all customers equally.

Using one year of online retail transaction data, the project performs data cleaning, exploratory data analysis (EDA), RFM (Recency, Frequency, Monetary) feature engineering, K-Means clustering, and statistical validation to discover meaningful customer segments.

The final output includes enriched datasets that can be imported into Power BI for dashboard development and business reporting.

---

## Repository Contents

```text
├── notebook.ipynb
├── online_retail_segmented.csv
├── executive_summary.md
├── dashboard.pbix
├── dashboard_screenshots
│    ├── page1_overview.png
│    └── page2_segments.png
└── README.md
```

---

## Technologies Used

- Python
- pandas
- NumPy
- Matplotlib
- Seaborn
- scikit-learn
- SciPy
- Jupyter Notebook
- Power BI (for downstream visualization)

---

## Reproduction Steps

### 1. Download the dataset

Place the file:

```text
online_retail.csv
```

in the same directory as the notebook.

The project uses the UCI Online Retail dataset containing transactions from December 2010 through December 2011.

### 2. Run the notebook

Execute the notebook sequentially from top to bottom.

The workflow consists of:

1. Data Engineering & Cleaning
2. Exploratory Data Analysis
3. RFM Feature Construction
4. K-Means Clustering
5. Statistical Validation
6. Customer Lifetime Value Estimation
7. Export for Power BI

### 3. Generated outputs

Running the notebook produces:

- Cleaned transaction dataset
- Customer-level RFM table
- Customer segment assignments
- Data visualizations
- Executive summary
- CSV exports for Power BI

---

## Methodology

### Data Cleaning

Several preprocessing steps were applied before analysis:

- Remove transactions with missing Customer IDs
- Remove returned or cancelled orders
- Remove duplicate records
- Convert invoice dates into datetime format
- Create a `TotalAmount` feature

### Exploratory Data Analysis

EDA was performed to understand customer purchasing behaviour and overall business performance.

The analysis includes:

- Revenue by country
- Top-selling products
- Revenue by month, day, and hour
- Customer spending distribution
- Customer order frequency distribution

### RFM Analysis

Three customer metrics were calculated:

| Metric | Description |
|----------|-------------|
| Recency | Days since the customer's last purchase |
| Frequency | Number of unique orders placed |
| Monetary | Total amount spent by the customer |

These features summarize customer behaviour and provide the foundation for segmentation.

### K-Means Clustering

RFM variables were standardized before clustering.

The optimal number of clusters was determined using:

- Elbow Method
- Silhouette Score

Customers were then assigned to business-friendly segments:

- Champions
- Loyal Customers
- At-Risk
- Lost / Hibernating

### Statistical Validation

An ANOVA test was performed to evaluate whether average customer spending differed significantly across the identified segments.

A supplementary linear regression model was also included to demonstrate understanding of the R² metric. Since K-Means is an unsupervised learning algorithm, silhouette score remains the primary evaluation metric, while R² is presented for educational completeness.

### Customer Lifetime Value (CLV)

A simple three-year Customer Lifetime Value estimate was calculated using:

```
CLV ≈ Average Order Value × Purchase Frequency × Customer Lifespan
```

This estimate highlights the long-term financial importance of retaining high-value customer segments.

---

## Key Findings

### 1. Revenue Concentration

The United Kingdom contributes the majority of total revenue, while several international markets represent smaller but potentially valuable growth opportunities.

### 2. Customer Spending Distribution

Customer spending is highly right-skewed. A relatively small number of customers generate a disproportionately large share of total revenue.

### 3. Seasonal Sales Patterns

Sales activity increases significantly during the holiday season, with November and December producing the highest revenues.

### 4. Customer Segmentation

RFM analysis combined with K-Means clustering successfully identifies distinct groups of customers with different purchasing behaviours.

These segments enable more effective marketing strategies by identifying:

- High-value customers to retain
- Loyal customers to develop further
- At-risk customers requiring intervention
- Inactive customers suitable for re-engagement campaigns

### 5. Statistical Evidence

Silhouette analysis supports the selected clustering solution, while ANOVA testing confirms statistically significant differences between customer segments.

---

## Business Recommendations

### Reward Champions

Offer loyalty incentives, early product access, and exclusive promotions to retain the highest-value customers.

### Win Back At-Risk Customers

Use targeted email campaigns and limited-time offers to encourage inactive customers to return.

### Upsell Loyal Customers

Promote premium products and bundles rather than relying on broad discounts.

### Improve Customer Retention

Retaining existing customers is generally more cost-effective than acquiring new ones, making segmentation-driven marketing a valuable business strategy.

---

## Summary

This project demonstrates a complete customer analytics workflow, transforming raw transaction data into actionable business insights.

By combining data cleaning, exploratory analysis, RFM modeling, K-Means clustering, and statistical validation, the project provides a practical framework for customer segmentation that supports data-driven decision making.

The exported datasets are designed for direct integration into Power BI, allowing interactive dashboards and ongoing business monitoring.

---

## Dataset

**Online Retail Dataset**

- Source: UCI Machine Learning Repository
- Period Covered: December 2010 – December 2011
- Business Type: UK-based online gift retailer

The dataset contains historical transaction records used to perform customer segmentation and marketing analysis.

