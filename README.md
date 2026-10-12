# Olist E-Commerce Data Analysis | Excel, Power Query & Power Pivot

## Project Overview

This project analyses the Brazilian Olist e-commerce dataset to explore sales performance, customer distribution, product performance, and order delivery efficiency.

The goal was to transform multiple related datasets into a structured analytical model and develop an interactive Excel dashboard that supports business decision-making.

The project covers the complete data analysis workflow, from data auditing and cleaning to data modelling, KPI development, visualisation, and interpretation.

## Business Objectives

The analysis addresses five main questions:

1. How do revenue and order volumes change over time?
2. Which product categories contribute most to revenue and sales volume?
3. How are customers distributed geographically?
4. How efficiently are customer orders fulfilled and delivered?
5. How does customer satisfaction vary across product categories, and is it associated with revenue performance?

## Tools and Technologies

| Tool | Application |
|---|---|
| Microsoft Excel | Data analysis, PivotTables, visualisations and dashboard development |
| Power Query | Data cleaning, transformation and validation |
| Power Pivot | Relational data modelling |
| DAX | Calculated measures and key performance indicators |
| PivotCharts and Excel Charts | Business performance visualisation |
| Excel Slicers | Interactive filtering by customer state |

## Dataset

**Source:** [Brazilian E-Commerce Public Dataset by Olist — Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

The dataset contains approximately 100,000 orders from a Brazilian e-commerce marketplace, alongside related information about customers, products, sellers, payments, reviews and geographical locations.

The analysis uses multiple linked tables, including customer records, orders, order items, products, sellers, product category translations and customer reviews.

## Data Preparation and Modelling

Data preparation was performed primarily using Power Query.

The process included:

- Auditing datasets for missing values, duplicate records and identifier uniqueness.
- Checking and correcting data types, including dates, numeric values and identifiers.
- Standardising text fields and retaining postcode prefixes as text.
- Investigating missing product attributes and delivery timestamps.
- Checking order-date sequences and identifying inconsistent records.
- Validating product prices and freight charges without automatically removing legitimate zero-freight transactions.
- Examining duplicate geographical records.
- Building relationships between datasets using their shared identifiers.

The cleaned tables were loaded into Excel's Data Model, where DAX measures were developed for revenue, order counts, average order value, sales volume, review scores and delivery performance.

## Dashboard

The interactive Excel dashboard combines four headline KPIs with six visualisations covering sales, customers, products and deliveries.

**Dashboard preview**

*Add a screenshot of the completed dashboard here.*

### Key Performance Indicators

| KPI | Result |
|---|---:|
| Total Revenue | R$ 16,003,842.91 |
| Total Orders | 99,421 |
| Average Order Value | R$ 160.91 |
| Delivery Completion Rate | 97.04% |

The dashboard includes a customer-state slicer that allows users to explore selected geographical differences. State-ranking comparisons and overall delivery summaries remain available as reference views.

## Key Findings

### 1. Sales and Revenue Trends

Order volumes increased considerably throughout 2017, with November recording 7,544 orders.

Monthly revenue and order volume followed broadly similar patterns, suggesting that changes in transaction volume were an important contributor to revenue growth.

The monthly analysis focuses on January 2017 to August 2018 to avoid misleading comparisons involving low-volume boundary months.

### 2. Product Category Performance

The `health_beauty` category generated the highest product revenue, approximately R$ 1.26 million.

Meanwhile, `bed_bath_table` recorded the highest order-item count, with 11,115 items.

The distinction between revenue and sales volume demonstrates that categories generating the most sales activity are not necessarily those generating the most revenue.

The `computers` category also recorded a particularly high average revenue per order item, approximately R$ 1,098, among categories meeting the minimum sales-volume threshold.

### 3. Customer Satisfaction

Product categories differed in their average customer review scores.

To reduce the influence of categories with very few reviews, a minimum threshold of 100 associated reviews was applied to the category-rating comparison.

The relationship between product-category revenue and average review score was extremely weak, with a linear R² value close to zero.

This suggests that higher category revenue was not consistently associated with higher customer ratings.

### 4. Delivery Performance

The dataset contained 96,478 orders marked as delivered.

Of the 96,476 orders with the necessary delivery dates, 7,827 arrived after their estimated delivery dates.

This corresponds to:

- **On-time delivery rate:** 91.89%
- **Late delivery rate:** 8.11%
- **Average actual delivery duration:** 12.56 days
- **Average estimated delivery duration for delivered orders:** 23.74 days

Actual deliveries were substantially faster than the estimated delivery windows on average, although a minority of orders arrived late.

### 5. Geographical Delivery Differences

Delivery performance varied across Brazilian states.

Alagoas (AL) recorded the highest late-delivery rate in the state comparison, at 23.93%, while Maranhão (MA) followed at 19.67%.

Rio de Janeiro (RJ) recorded 1,664 late deliveries, demonstrating that states with lower late-delivery percentages can still contribute substantially to the total number of delayed orders.

These findings highlight the importance of examining both delivery rates and order volumes.

## Business Recommendations

**Improve delivery performance in high-delay regions.** Investigate the operational factors associated with elevated late-delivery rates, prioritising states with both high delay percentages and meaningful order volumes.

**Monitor customer satisfaction alongside sales.** Revenue alone does not provide a complete picture of product-category performance. Review scores and review counts should complement financial KPIs.

**Plan for periods of high demand.** Strong order volumes during November 2017 suggest that the business could benefit from examining promotional periods and preparing fulfilment capacity accordingly.

**Use geographical insights to guide operational decisions.** Differences in delivery duration and punctuality suggest that state-level monitoring could support logistics planning and service improvements.

## Limitations

- The dataset is historical and does not represent current marketplace performance.
- Some date and product fields contain missing values.
- Certain order timestamps have sequence inconsistencies.
- The available data covers incomplete calendar periods, limiting seasonal comparisons.
- Review averages based on small samples may be unstable.
- Observed relationships should not be interpreted as evidence of causation.
- Order-item counts measure item records rather than a separate quantity field.

## Conclusion

This project demonstrates how Excel, Power Query, Power Pivot and DAX can be combined to analyse a multi-table e-commerce dataset and develop an interactive business intelligence dashboard.

The analysis identifies important differences between sales volume and revenue, highlights geographical variation in delivery performance, and demonstrates why customer satisfaction should be considered alongside commercial performance.

The completed dashboard provides an accessible way to explore these findings and support data-informed business decisions.
