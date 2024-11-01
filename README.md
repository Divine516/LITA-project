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
