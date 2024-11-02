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


After all these anaysis on excel spreadsheet, we saved our file using csv(comma delimited format) to our documented and proceeded to our Structured Query Language (SQL) to write queries to: 

- retrieve the total sales for each product category.
- find the number of sales transactions in each region.
- find the highest-selling product by total sales value.
- calculate total revenue per product.
- calculate monthly sales totals for the current year.
- find the top 5 customers by total purchase amount.
- calculate the percentage of total sales contributed by each region.
- identify products with no sales in the last quarter.
