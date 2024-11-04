# Project name: LITA_Capstone_Project.

This is a documentation of data validation, cleaning, querying, transformation, and visualization I carried out while working on the Sales Data of  Ladies in Tech Africa's final project.  

## Topic: Sales Data Analysis.

### Overview
---
This project collects and analyzes sales trends of some products from various regions from January 2023 to August 2024. This project aims to generate key insights such as top-selling products, regional performance, customer behavior, and monthly sales trends.

### Data Collected
---
The dataset includes the following key columns:

- OrderID: The identification number attached to each order.
- Customer Id: A unique identification number given to each customer,
- Product: The product being sold.
- Region: The geographical area where the products are being sold.
- OrderDate: The date of each product purchase.
- Quantity: The number of products each customer purchases per transaction.
- UnitPrice: The amount of each product.

### Tools Used
---
1. Microsoft Excel: For Data Cleaning, Analysis, and Visualization.
2. Structured Query Language(SQL): For Querying of Data.
3. Power BI: For Data Transformation, and Virtualization. 

### Data Cleaning and Preparations
---
The following actions were performed to clean and prepare the data:

- Data Loading and Inspection on Microsoft Excel, SQL, and Power BI.
- Data Cleaning and Formatting on Microsoft Excel and Power BI.
- Handling and Calculating missing variables on Microsoft Excel, SQL, and Power BI.

### Exploratory Data Analysis
---
The data was explored to determine the following: 
- Total sales by product, region, and month.
- Average sales per product.
- Total revenue by region.
- Total sales for each product category.
- Number of sales transactions in each region.
- Highest-selling product by total sales value.
- Total revenue per product.
- Monthly sales totals for the year 2024.
- Top 5 customers by total purchase amount.
- Percentage of total sales contributed by each region.
- Products with no sales in the last quarter.
- Regional breakdowns

### Data Analysis, Visualization, and Inferences (Microsoft Excel)
---
This includes all the pivot tables made using Microsoft Excel.
1.	Total Sales per Product

### Data Analysis, Visualization, and Inferences (SQL)
---
This includes the lines of queries used during the analysis using SQL.
1.	Total sales of each product category.

```SQL
select sum(sales) as total_sales, product from [dbo].[Capstone Sales Data]
group by product
```

![SQL 1 1](https://github.com/user-attachments/assets/b15afd34-24bd-4f18-ab72-e7031631066a)

