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
This includes the lines of queries used during the analysis using SQL, and their outputs.
#### 1.	Total sales of each product category.

```SQL
select sum(sales) as total_sales, product from [dbo].[Capstone Sales Data]
group by product
```

![SQL 1 1](https://github.com/user-attachments/assets/b15afd34-24bd-4f18-ab72-e7031631066a)

#### Inference:

#### 2.	Number of sales transactions in each region. 

```SQL 
select count(orderid) as Sales_Count, Region from [dbo].[Capstone Sales Data]
GROUP BY Region
```

![SQL 1 2](https://github.com/user-attachments/assets/f3671ef6-386a-439f-a849-c76c9b25bb58)

#### Inference:

#### 3.	Highest-selling product by total sales value.

```SQL 
select top 1 sum(sales) as Highest_Selling_Product, product from [dbo].[Capstone Sales Data]
group by product
```

![SQL 1 3](https://github.com/user-attachments/assets/cfbdc12a-ffd7-4a16-b808-2c7580d7da70)

####Inference:

#### 4.	Total revenue per product.

```SQL 
select sum(sales) as total_revenue,
product from [dbo].[Capstone Sales Data]
group by product
```

![SQL 1 4](https://github.com/user-attachments/assets/36c29966-4560-4fbb-aa03-9902f8f377e4)

#### Inference:

#### 5.	Monthly sales totals for the current year.

```SQL 
select sum(sales) as Sales_2024, Month from [dbo].[Capstone Sales Data]
where year =2024
group by month  
```

![SQL 1 5](https://github.com/user-attachments/assets/eeed5836-541b-4afd-a52f-0d7198e9b4da)

#### Inference:

#### 6.	Top 5 customers by total purchase amount.

```SQL 
select top 5 sum(sales) as Top_5, Customer_Id from [dbo].[Capstone Sales Data]
group by Customer_Id 
```

![SQL 1 6](https://github.com/user-attachments/assets/6272b82f-2052-4811-a591-1ab830253761)

#### Inference:

#### 7.	Percentage of total sales contributed by each region.

```SQL 
select region, 
sum(sales) as Region_Sales,
count(sales) *100.0/sum(count(sales)) over () as Percentage from [dbo].[Capstone Sales Data]
group by region 
```

![SQL 1 7](https://github.com/user-attachments/assets/53172187-c0bd-4093-b8dd-89ff3be78795)

#### Inference:

#### 8.	Products with no sales in the last quarter.

```SQL 
select Product from [dbo].[Capstone Sales Data]
where sales=0
  and year =2024
and quarter =3
```

![SQL 1 8](https://github.com/user-attachments/assets/8c531a35-b8bb-4dcd-ad9a-69df2ecf47e2)

#### Inference:




