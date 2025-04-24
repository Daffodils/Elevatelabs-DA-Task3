# Elevatelabs-DA-Task3
Task 3: SQL for Data Analysis Objective: Use SQL queries to extract and analyze data from a database.


# Walmart Sales Analysis  

## Project Overview  
This project involves analyzing the Walmart sales dataset to derive insights and patterns based on sales transactions. Using SQL queries, we explore various aspects of the dataset, including product sales, customer demographics, and revenue generation.  

## Objective  
The primary goal of this analysis is to manipulate and query structured data using SQL to gain insights from the Walmart sales dataset. This project serves to enhance understanding of SQL functionalities such as aggregations, joins, and data filtering.  

## Dataset  
The analysis utilizes the *Sales* table which contains transactional data from Walmart. The table includes the following fields:  

- **Invoice_ID**: Unique identifier for each transaction.  
- **Branch**: The branch of Walmart where the sale occurred.  
- **City**: The city where the branch is located.  
- **Customer_type**: Classification of customers (e.g., Member or Non-Member).  
- **Gender**: Gender of the customer.  
- **product_line**: Category of the product sold.  
- **unit_price**: Price per unit of the sold product.  
- **quantity**: Number of units sold.  
- **VAT**: Value-added tax applied.  
- **Total**: Total cost of the transaction.  
- **date**: Date of the transaction.  
- **Time**: Time of the transaction.  
- **Payment_cogs**: Type of payment transaction (e.g., Cash, Credit card).  
- **COGS**: Cost of goods sold.  
- **gross_margin_pct**: Gross margin percentage.  
- **Gross_income**: Total income from sales.  
- **Rating**: Customer rating of the product.  

## SQL Queries  
### Existing Queries  
1. **How many unique cities does the data have?**  
    ```sql  
    SELECT DISTINCT city FROM sales;  
    ```  

2. **In which city is each branch?**  
    ```sql  
    SELECT DISTINCT city, branch FROM sales;  
    ```  

3. **How many unique product lines does the data have?**  
    ```sql  
    SELECT COUNT(DISTINCT product_line) FROM sales;  
    ```  

4. **What is the most selling product line?**  
    ```sql  
    SELECT product_line, COUNT(Invoice_ID) AS CNT   
    FROM sales   
    GROUP BY product_line   
    ORDER BY CNT DESC   
    LIMIT 1;  
    ```  

5. **What is the total revenue by month?**  
    ```sql  
    SELECT DATE_FORMAT(date, '%Y-%m') AS month, SUM(Total) AS total_revenue   
    FROM sales   
    GROUP BY month   
    ORDER BY total_revenue DESC;  
    ```  
## Conclusion  
This project demonstrates the ability to analyze structured data using SQL effectively. The insights gained from the analysis has helped me in understanding sales patterns and customer behaviors to make informed business decisions.
