# DSA3050A Mid-Semester Practical Examination

**Student Name:** Ruth Musanhu
**Student ID:** 670474

## Project Title

Olist E-Commerce Sales and Delivery Analysis


## Dataset Source

**Dataset:** Brazilian E-Commerce Public Dataset by Olist
**Source:** Kaggle
**Source URL:** https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

The original dataset files were downloaded from Kaggle and retained without artificial modification, fabrication, or row inflation.

## Dataset Size

The final Power BI model contains:

* **Sales_Fact:** 115,011 rows and 37 columns
* **DateTable:** 774 rows and 6 columns

The main dataset used for business analysis is `Sales_Fact`.

## Business Problem

Olist management needs a clear view of sales performance, customer purchasing patterns, product-category performance, payment behaviour, regional demand, delivery performance, and customer satisfaction.

The purpose of this Power BI project is to clean and transform the raw e-commerce data, then develop an interactive dashboard that helps management:

* Monitor total sales, total orders, and average order value
* Identify high-performing product categories and customer regions
* Analyse sales trends over time
* Understand the most commonly used payment methods
* Compare customer review ratings against the target
* Support data-driven operational and commercial decisions

## Power Query Transformations Performed

### Basic Data Cleaning

* Renamed unclear columns using descriptive business names
* Assigned correct text, date/time, whole-number, and fixed-decimal data types
* Removed duplicate order, customer, product, seller, and review records
* Removed blank rows
* Trimmed and cleaned text columns
* Standardised text using uppercase, title case, and replacement of inconsistent payment values
* Removed unnecessary columns from the final fact table

### Intermediate Transformations

* Split `LocationToSplit` into customer city and customer state columns
* Merged customer city and state into `CustomerLocation`
* Created `ItemTotalValue` and `DeliveryDays` custom columns
* Created `DeliveryStatus` and `SalesValueCategory` conditional columns
* Extracted year, month, quarter, and day from the purchase date
* Filtered orders using order status and delivery-day conditions
* Sorted records by purchase date and payment sequence
* Added an index column to the cleaned orders table

### Advanced Transformations

* Merged orders, customers, products, category translations, sellers, payments, and reviews using common keys
* Created a dynamic date table in Power Query
* Used Group By with multiple aggregations for payment and review summaries
* Created nested business-value categories
* Created summarized and supporting queries using Reference Query
* Used column profiling to inspect quality, distribution, null values, and errors
* Handled errors in calculated sales values
* Expanded merged query columns into the final `Sales_Fact` table


## Dashboard Visuals Created

* Card for Total Sales Revenue
* Card for Total Orders
* Card for Average Order Value
* KPI visual for Average Review Rating versus Target
* Clustered bar chart for Sales by Product Category
* Clustered column chart for Sales by Customer State
* Line chart for Sales Trend Over Time
* Donut chart for Orders by Payment Type
* Table visual for Product Category Performance
* Matrix visual for Sales by State and Product Category
* Map visual for Sales by Customer Location
* Treemap for Sales Contribution by Product Category
* Year slicer
* Customer State slicer
* Product Category slicer

## Business Insights

1. **Health and beauty was the highest-performing product category**, generating approximately R$1,456,170 in total sales. This suggests that the category is a major revenue driver and should receive strong inventory, marketing, and supplier support.
2. **São Paulo (SP) was the strongest customer market**, generating approximately R$6,041,485 in total sales. This indicates that SP is Olist’s most important regional market and should remain a priority for customer retention, logistics capacity, and targeted marketing.
3. **Credit cards were the dominant payment method**, accounting for 74,284 orders, or 75.31% of all orders. This shows that Olist depends heavily on card payments, making reliable payment processing and card-related promotions important to the business.


