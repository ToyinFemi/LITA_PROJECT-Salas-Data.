# Project name: LITA_Capstone_Project: Sales Performance Analysis for a Retail Store.
---
This is a documentation of data validation, cleaning, querying, transformation, and visualization I carried out while working on the Sales Data of  Ladies in Tech Africa's final project.  

## Topic: Sales Performance Analysis.
---

[Project Overview](#project-overview)

[Data Collected](#data-collected)

[Tools Used](#tools-used)

[Data Cleaning and Preparation](#data-cleaning-and-preparation)

[Exploratory Data Analysis](#exploratory-data-analysis)

[Data Visualization](#data-visualization)

[Inference](#inference)

### Project Overview
---
This project collects and analyzes sales trends of products sold by  a retail store that has outlets in different regions from January 2023 to August 2024. This project aims to generate key insights such as top-selling products, regional performance, customer behavior, and monthly sales trends.

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

The following are the calculated columns made in Excel:
- Sales.
Formula used: = Quantity * Unit Price
  
- Year.
Formula used: = Year (OrderDate)
  
- Month.
Formula used: = TEXT (OrderDate, "Mmm")
  
- Quarter. 
Formula used: = =ROUNDUP (MONTH(OrderDate)/3,0)
---

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


### Data Visualization
(Microsoft Excel)
---
This includes all the pivot tables made using Microsoft Excel.
#### 1.	Total Sales per Product.

![X 1 1](https://github.com/user-attachments/assets/ce51a231-52a5-4bfd-b7ec-d6ccbb187ba6)

#### 2.	Total Sales per Region.

![X 1 2](https://github.com/user-attachments/assets/a758af49-bf13-4194-a3c1-ca309b289495)

#### 3.	Total Sales per Month.

![x 1 3](https://github.com/user-attachments/assets/e99248d0-c5a4-444b-a000-55ca866dcbe5)

#### 4. Average Sales per Product.

![x 1 4](https://github.com/user-attachments/assets/7edb54db-ba72-48cc-8e9d-5d1e99023145)

#### 5. Total Revenue by Region. 

![x 1 5](https://github.com/user-attachments/assets/eda253d5-6874-4bf5-8b77-08c4140cc2f1)
---


### Data Visualization
(SQL)
---
This includes the lines of queries used while analyzing the data on SQL, and their outputs.

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


### Data Visualization
(Power BI)
---
This includes all the Visuals made using Power BI.

![PBI 1 1](https://github.com/user-attachments/assets/ac029179-86a6-4a9f-99d4-46963d37fe37)

![PBI 1 2](https://github.com/user-attachments/assets/a62c8973-9c0e-483c-9565-f185cf5165e7)

![PBI 1 3](https://github.com/user-attachments/assets/1e5e5f56-aea3-4410-aec3-710a8310a8e1)

![PBI 1 4](https://github.com/user-attachments/assets/474fa775-ae10-4862-91e9-b655d85aab1b)

![PBI 1 5](https://github.com/user-attachments/assets/692d4ac7-1be1-4500-87f5-b76b6af3ddd2)

![PBI 1 6](https://github.com/user-attachments/assets/6fbe3eaf-821e-4f47-991c-54985c2a5f06)

![PBI 1 7](https://github.com/user-attachments/assets/e49aa4a8-707f-4ddf-af32-d8d172e6820a)

![pbi 1 8](https://github.com/user-attachments/assets/5412335a-1be9-47f7-a17d-99b37c40fa12)

![PBI 1 9](https://github.com/user-attachments/assets/024f62ee-24c7-4e4c-9a4c-d49227b2b0a1)

![PBI 1 10](https://github.com/user-attachments/assets/cb5e4d57-966d-4873-a6f6-53daab24de0d)

![PBI 1 11](https://github.com/user-attachments/assets/c7ae8d97-0b28-487c-bd66-91374f1582e8)

![PBI 1 12](https://github.com/user-attachments/assets/06909885-cd5b-4ba2-a77b-4486fbbcbfa5)

![PBI 1 13](https://github.com/user-attachments/assets/1d1b6f37-1bb8-4baf-b765-1842e888bd8c)

![PBI 1 14](https://github.com/user-attachments/assets/7183074c-b281-4198-8da5-ec506254698d)

![PBI 1 15](https://github.com/user-attachments/assets/e3dd7b58-dbeb-415e-850d-f0c40050cab5)

---

### Inference


