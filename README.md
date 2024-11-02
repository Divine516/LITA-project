# CAPSTONE DATA ANALYSIS PROJECT (SALES DATA)
## CONTENT OF THE SALES DATA EXCEL SPREADSHEET
- OrderID
- CustomerID
- Product
- Region
- OrderDate
- Quantity
- Unit Price

We have been tasked with analyzing the sales performance of a retail store. Let the retail store be known as Melewis Boutique. 
The sales performance includes:
- the total sales by product, region, and month
- average sales per product
- total revenue by region
We will also be using pivot tables and pie chart to summarize the total sales by product, region, and month. Furthermore, after analyzing this data set on excel worksheet, we will be importing into Structured Query Language(SQL) to run queries on the data and then proceed to Power Business Intelligence(Power BI) for visualization of the data set.
This data set  has a total of 50,001 rows and 7 columns to be worked on and this data set is clean.

To get the total sales of each product, you first have to get the total sale per OrderID or CustomerID. That is the (unity price* Quantity) for the OrderID or CustomerID on each row. 

![sales data 1](https://github.com/user-attachments/assets/65a4f168-eeda-412d-b73b-fb817c151381)

A pivot table to summarize the total sales by product, region, and month of the data set is created. The grand total sales made between January 2023 and December 2024 is 10,587,500 and the breakdown of the total sales per product is as follows:

- Gloves   = 1,500,00
- Hat      = 1,587,500
- Jacket   = 1,050,000
- Shirt    = 2,450,000
- Shoes    = 3,087,500
- Socks    = 912,500

The product that brought in the highest revenue is Shoes with a total of 3,087,500 and the product that brought in the lowest revenue is Socks with a total of 912,500.

The total sales per region breakdown is as follows:

- East = 2,450,000
- North = 1,950,000
- South = 4,675,000
- West = 1,512,500

The region with the highest sales is the Southern region with a total of  4,675,000 and the region with the lowest sales is the wesstern region with a total of 1,512,500.

The total sales per month for both 2023 and 2024 breakdown is as follows:

- January = 1,250,000
- Feburary = 2,750,000
- March = 537,500
- April = 237, 500
- May = 525,000
- June = 1,250,000
- July = 1,387,500
- August = 1,025, 000
- September = 175,000
- October = 675,000
- November = 525,000
- December = 250,000

The month with the highest sales is Feburary with a total of 2,750,000 and the month with the lowest sales is April with a total sales of 237,500.

![Project Excel 1](https://github.com/user-attachments/assets/c2f6bd65-a92c-4940-a596-3f6e73c36936)



Pie charts are used to show this data set for quicker analysis

![Project Excel 2](https://github.com/user-attachments/assets/cc663d87-3b55-4510-aa00-d94860ca695b)


![Project Excel 2-1](https://github.com/user-attachments/assets/4abf8a8b-3a5f-4e9c-a9d1-2c7c630ea195)



Formulas were also used to find the average sales per prodct and total sales per region. The averageif function was used to find the average sales per product and the sumif function for the total sales per region.  Also went ahead to look for more information that will help with our anlysis such as te hghest number of quantity sold, the lowest number of quantity sold, the fourth highest total sales, the fiftiest lowest total sales made and the overall number of sales made within 2023 ad 2024.



The average sales per product is as follows:

- Gloves = 200
- Hat = 158.75
- Jacket = 140
- Shirt = 326.6667
- Shoes = 308.75
- Socks = 121.6667

The total sales per region breakdown as already been stated above.

Futher analysis breakdown:

- The highest number of quanity sold = 12
- The lowest number of quantity sold = 2
- The fourth highest total sales = 600
- The fiftiest lowest total sales = 15
- Total number of sales made = 50,000



![sales data 2](https://github.com/user-attachments/assets/9a210e55-fc53-46bb-ad10-63fa70d46ded)





### SQL ANALYSIS

After all these anaysis on excel spreadsheet, we saved our file using csv(comma delimited format) to our documented and proceeded to our Structured Query Language (SQL) to write queries to: 

- retrieve the total sales for each product category.
- find the number of sales transactions in each region.
- find the highest-selling product by total sales value.
- calculate total revenue per product.
- calculate monthly sales totals for the current year.
- find the top 5 customers by total purchase amount.
- calculate the percentage of total sales contributed by each region.
- identify products with no sales in the last quarter.


The first step is the creation of the database "Capstone_Project" on our SQL maagement studio. 
Import the excel table to be used for the data squery to the SQL studio. 

Thereafter ``` SQL SELECT * FROM SALES DATA 2-1-2``` and begin to write queries to analyze your data set. The first query to be written is to 

1. Retrieve the total sales for each product category : ```SQL select product, sum(Total_Sales) as product_total_sales from [dbo].[Sales Data-2-1-2]
Group by PRODUCT```. The total sales retrieved is as follows :

- Shoes =	3,087,500
- Jacket =	1,050,000
- Hat	= 1,587,500
- Socks =	912,500
- Shirt	= 245,0000
- Gloves =	1,500,000

In addition to the total sales for each product category, further analysis was made on total quantity that was sold for each product: ```SQL select product, sum (Quantity) as Quantity_Revenue from [dbo].[Sales Data-2-1-2]
Group by product```. The total quantity per product is as follows:

- Shoes = 72,500
- Jacket = 27,500
- Hat = 80,000
- Socks = 40,000
- Shirt = 62,500
- Gloves = 62,500


![sql 1](https://github.com/user-attachments/assets/b7c374a3-0d47-4c0b-bf8f-be6c09e222b2)


2. Find the number of sales transactions in each region: ```SQL select Region, count (CustomerID) as sales_by_region from [dbo].[Sales Data-2-1-2]
Group by Region```. The total number of sales transaction are as follows:

 - North =	12,500
 - East	= 12,500
 - South = 12,500
 - West =	12,500

3. Find the highest-selling product by total sales value: ```SQL select product, sum (Total_Sales) as product_total_sales from [dbo].[Sales Data-2-1-2]
Group by product
order by product_total_sales desc``` . The highest selling product in descending order is as follows:

- Shoes =	3,087,500
- Shirt =	2,450,000
- Hat = 1,587,500
- Gloves = 1,500,000
- Jacket = 1,050,000
- Socks =	912,500


![sql 2](https://github.com/user-attachments/assets/5c51594b-6d73-4f10-8346-e5989bd39ed8)




4. Calculate total revenue per product: ``SQL select product, sum (Total_Sales) as product_total_sales from [dbo].[Sales Data-2-1-2]
Group by product```. The total revenue for each product is as follows:

- Shoe = 3,087,500
- Jacket =	1,050,000
- Hat =	1,587,500
- Socks	= 912,500
- Shirt =	2,450,000
- Gloves =	1,500,000


5. Calculate monthly sales totals for the current year:```SQL select orderdate, sum (Total_sales) as Totalsales from [dbo].[Sales Data-2-1-2]
where orderdate >= '2024-01-01'
group by orderdate```. The monthly sales total is as follows:

- 2024-07-31 =	187,500
- 2024-04-30 =	200,000
- 2024-06-30	= 750,000
- 2024-03-31 =	275,000
- 2024-02-29	= 1,500,000
- 2024-01-31	= 1,000,000
- 2024-05-31 =	225,000
- 2024-08-31	= 875,000 

6. Find the top 5 customers by total purchase amount: ```SQL select CustomerID, sum (Total_sales) as Totalsales from [dbo].[Sales Data-2-1-2]
group by CustomerID
order by Totalsales desc```. The top 5 customers are:

- Cus1488	= 29,340
- Cus1375	= 28,925
- Cus1023	= 28,205
- Cus1059	= 28,005
- Cus1367	= 27,920


![sql 3-1](https://github.com/user-attachments/assets/67fcd030-2b16-423b-ae4f-700fa1f11330)


7.  Calculate the percentage of total sales contributed by each region: ```SQL SELECT Region, SUM(Total_sales) AS RegionalSales,
(SUM(Total_sales) / CAST((SELECT SUM (Total_sales) FROM [dbo].[Sales Data-2-1-2])
AS DECIMAL(10, 2)) * 100) AS SalesPercentage
FROM [dbo].[Sales Data-2-1-2]
GROUP BY Region```. The total perentage is:

Region/ Regional Sales/ Sales Percentage 
- North/	1950000/	18.41794569000
- East/ 2450000/	23.14049586700
- South/	4675000/ 44.15584415500
- West/	1512500/	14.28571428500


![sql 4](https://github.com/user-attachments/assets/a5f72d71-fb82-479d-8730-0a113243f45d)


8. Identify products with no sales in the last quarter: ```SQL SELECT DISTINCT Product FROM [dbo].[Sales Data-2-1-2]
WHERE product Not In (select product from [dbo].[Sales Data-2-1-2]
Where OrderDate >= dateadd (quarter, -1, getdate ()) )```. Products with no sales in the last quarter:

- Gloves
- Jacket
- Shirt
- Shoes
- Socks


![sql 5](https://github.com/user-attachments/assets/aff5f3bc-9b2f-444a-9288-7f89beee12f7)


