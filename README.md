# Product Sales Analysis Using Power BI (Version 2.0)

## Project Overview

This project is an improved and visualized version of my previous SQL sales analysis project involving approximately **50,000 sales transactions** from a **multichannel product dataset**. The project extends the previous analysis by transforming key findings into an interactive Power BI dashboard covering sales performance, products and customers, returns, sales channels, and operational activities.

## Objectives
- Determine monthly sales revenue trends.
- Identify product and category rankings using different performance metrics.
- Evaluate performance across returns, sales channels, payment methods, shipping, warehouses, and order priorities.
- Compare performance metrics to identify meaningful patterns and differences.
- Develop insights and business recommendations based on the analysis.
- Tools & Technologies
- PostgreSQL
- Microsoft Power BI
- DAX
- Star Schema Modeling
- Dataset

The dataset was sourced from **Kaggle** and contains approximately **50,000 sales transactions involving online and in-store** transactions. It includes information on **products**, **categories**, **countries**, **sales channels**, **payment methods**, **shipping providers**, **warehouses**, **order priorities**, **returns**, **quantities**, **prices**, **discounts**, and **transaction dates**.

The dataset is synthetic; therefore, the findings are intended to demonstrate analytical methodology rather than represent the actual performance of a real company.

## Data Preparation & Modeling

The dataset underwent inspection, cleaning, and preparation before analysis.

Key preparation steps included:

- Data import and initial inspection in Power BI.
- Duplicate inspection and removal.
- Replacement of the original category field with a cleaned category classification.
- Identification and separate classification of negative transactions.
- Preparation of relevant fields for measures, slicers, and visualizations.

The Power BI model follows a **star schema**, with **FactSales** as the central transaction-level fact table and dimension tables providing analytical context.

Key dimensions include:

- Date
- Product and Category
- Country
- Sales Channel
- Payment Method
- Shipment Provider
- Warehouse Location
- Order Priority
- Return Status

The model enables consistent filtering and cross-analysis across the dashboard.

## Measures & Analytical Approach

The analysis uses multiple measures to evaluate performance from different perspectives:

- **Positive Revenue** — revenue from positive sales transactions, excluding negative transactions from the primary sales analysis.
- **Calculated Revenue** — revenue calculated across the transaction data.
- **Invoice Count** — transaction volume based on distinct invoices.
- **Average Order Value (AOV)** — average revenue generated per invoice.
- **Return Rate** — frequency of transactions associated with returns.
- **Returned Revenue** — financial value associated with returned transactions.
- **Shipping and Operational Measures** — used to compare shipping and warehouse/order activity.

The analytical approach followed:

```mermaid
flowchart LR
    A[Business Question] --> B[Select Metric]
    B --> C[Analyze by Dimension]
    C --> D[Compare Results]
    D --> E[Identify Patterns]
    E --> F[Validate Results]
    F --> G[Interpret Findings]
    G --> H[Develop Recommendations]
```

This approach was used to avoid relying on a single metric when evaluating performance.

## Dashboard Overview

The Power BI dashboard consists of six pages:

**1. Product Sales Performance**

Provides an overview of sales performance across products, markets, and time using revenue, invoice count, and AOV.

**2. Product & Customer Analysis**

Compares product, category, and country performance across revenue, invoice count, and AOV.

**3. Returns & Revenue Impact**

Examines return rate and returned revenue across products and categories.

**4. Sales Channel & Operations**

Compares sales channels, payment methods, and shipping providers using revenue, invoice count, AOV, and shipping metrics.

**5. Warehouse & Order Operations**

Analyzes warehouse activity, order priorities, and negative transaction activity.

**6. Business Insights & Recommendations**

Summarizes major findings and provides recommendations based on the observed results.

## Key Findings

- **Electronics** ranked highest in positive revenue among categories, while **Apparel** ranked lowest.
- **Germany** generated the highest revenue among the analyzed countries, while **Italy** ranked lowest.
- **White Mug** ranked first in both **positive revenue and AOV**, while product rankings differed when evaluated by invoice count.
- **Stationery** had the highest category return rate, while **Furniture** had the highest returned revenue.
- **Backpack** had the **highest product return rate**, while **USB Cable** had the **highest returned revenue**.
- **Online** ranked **highest in positive revenue and invoice count**, while **In-store** had the **highest AOV**.
- **Bank Transfer** ranked first across **positive revenue**, **invoice count**, and **AOV**, although the payment-method results were relatively close.
- **FedEx** ranked highest in **invoice count** and **total shipping cost**, while **Royal Mail** had the **highest average shipping cost per invoice**.
- **Amsterdam** recorded the highest invoice count among warehouse locations.
- **Medium order priority** ranked highest in invoice count, positive revenue, and AOV.
- **2,489 negative transactions**, representing approximately **5.0%** of the **49,782 transaction records**, were identified and separately classified.

## Business Recommendations

Based on the observed results, the analysis recommends:

- Investigating factors associated with higher product and category return activity.
- Examining Royal Mail's relatively high average shipping cost per invoice.
- Evaluating opportunities to increase in-store transaction volume while maintaining its higher AOV.
- Strengthening data validation and input controls to minimize negative transactions and other data-quality issues.
- Investigating potential relationships between discounts and revenue, AOV, invoice count, and return activity.

## Data Quality & Limitations
- The dataset is synthetic and sourced from **Kaggle**.
- Duplicate records were inspected and removed where necessary.
- A category data-quality issue required replacement with a cleaned category field.
- **2,489 negative transactions** (~5.0% of transaction records) were identified and analyzed separately.
- Transaction records and distinct invoices represent different measures.
- Several metrics rely on defined analytical assumptions, including Positive Revenue, Return Rate, and Returned Revenue.
- Observed relationships represent patterns or associations and do not establish causation.
- Findings demonstrate analytical methodology rather than actual business performance.

## Project Files

```mermaid
flowchart TD
    A[Product Sales Performance Analysis]

    A --> B[Data Analysis]
    A --> C[Power BI Dashboard]
    A --> D[Project Documentation]

    B --> B1[PostgreSQL]
    B --> B2[Product Sales Analysis SQL]

    C --> C1[Product Sales Performance]
    C --> C2[Product & Customer Analysis]
    C --> C3[Returns & Revenue Impact]
    C --> C4[Sales Channel & Operations]
    C --> C5[Warehouse & Order Operations]
    C --> C6[Business Insights & Recommendations]

    D --> D1[README.md]
    D --> D2[Paginated Report]
    D --> D3[Case Study]

    C --> E[Dashboard Screenshots]
```

## Dashboard Preview

![Product Sales Performance](Product%20Sales%20Performance%20Analysis/Screenshots/01_product_sales_performance.png)


![Product & Customer Analysis](Product%20Sales%20Performance%20Analysis/Screenshots/02_product_customer_analysis.png)


![Returns & Revenue Impact](Product%20Sales%20Performance%20Analysis/Screenshots/03_returns_revenue_impact.png)



![Sales Channel & Operations](Product%20Sales%20Performance%20Analysis/Screenshots/04_sales_channel_operations.png)


![Warehouse & Order Operations](Product%20Sales%20Performance%20Analysis/Screenshots/05_warehouse_order_operations.png)



![Business Insights & Recommendations](Product%20Sales%20Performance%20Analysis/Screenshots/06_business_insights_recommendations.png)

## Project Documentation

For a detailed discussion of the data preparation, data modeling, analytical approach, key findings, business recommendations, and project limitations, see the full project case study:

[View the Product Sales Performance Analysis Case Study](Product%20Sales%20Performance%20Analysis/Documentation/Product_Sales_Performance_Analysis_Case_Study.pdf)


## Conclusion

This project extended my previous SQL analysis into an interactive Power BI dashboard and provided practical experience in data preparation, modeling, DAX, visualization, analysis, and business-oriented interpretation. It strengthened my analytical foundation and gave me a clearer understanding of how to approach future data analytics projects.
