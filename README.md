
## Sales Insights Data Analysis Project

### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`


Data Analysis Using Power BI
============================

1. Formula to create norm_amount column

`= Table.AddColumn(#"Filtered Rows", "norm_amount", each if [currency] = "USD" or [currency] ="USD#(cr)" then [sales_amount]*75 else [sales_amount], type any)`


The Sales Insights Data Analysis project focuses on analyzing sales data to uncover key trends, patterns, and actionable insights to drive business decisions. This project involves cleaning and transforming raw sales data, creating visualizations, and generating dashboards to provide a comprehensive overview of sales performance.

💡 Project Overview:
The Sales Insights Data Analysis Project focuses on extracting, cleaning, and analyzing a dataset containing sales transactions across various regions, products, and time periods. The primary goal of this project is to uncover trends, improve sales strategies, and help stakeholders make data-driven decisions.

The project involves performing data cleaning, applying statistical techniques to analyze performance metrics, and creating interactive dashboards that provide clear, actionable insights. These insights help businesses optimize their revenue streams, identify high-performing products, and improve customer segmentation.

🔍 Key Objectives:
Analyze total revenue, profit, and sales growth across different regions.
Identify best-selling products and their contribution to overall sales.
Analyze customer purchasing patterns and behavior.
Provide actionable insights to improve marketing and sales strategies.
Create interactive dashboards for stakeholders using Power BI.
