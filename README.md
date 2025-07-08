# E-commerce-Sales-Analysis
## **Overview**
The objective of this analysis is to evaluate sales performance, identify trends, and provide actionable insights. The analysis focuses on sales data from an e-commerce platform, covering customer behavior, product performance, and revenue trends.

##
**Objectives**:
-	Understand overall sales performance
-	Identify best-selling products and customer purchase behavior
-	Categorized customer segment
-	Analyze sales trends over time

## **Tools Used**
- SQL Server
- Power bi(visualization)
-  Microsoft Word (document codes &summary)
-  
## **Data Collection**
Source: Data was extracted from the e-commerce platform, The analysis covers data from 
2nd January 2020 to 29th December 2022.

## **Key Tables:**
-	Orders: Order ID, Customer ID, Order Date, Total revenue
- Customers: Customer ID, Location, Customer Segment
- Products: Product ID, Category, Price

## **Methodology**
1.	Data Extraction: SQL queries were used to extract relevant data.
2.	Feature engineering: derived new column from existing column (power query).
3.	Analysis: Performed descriptive statistics using (Sql)
4.	Visualization: for proper interpretation and visualization using Power bi, DAX

### **Query example**
SELECT SUM(T_price) as Total_revenu from (select
o.product_id,product_name,product_price, quantity ,(quantity*product_price) as T_price
from 
orders o
join products p
on o.product_id=p.product_id) as sub_query
                     
## **Key Findings**
## 1. Overall Sales Performance
- The Total Revenue: $24,904,000
- Total Orders: 1000
- Total quantity sales: 50,000
- Average number of products included in each order: 50 products
- Average order value: $24,900
- The total number of customer is 1000, but only 615 customers orders during the period of this analysis customer’s Churn rate: 38.50% 
## 2. Top-Selling Categories
1.	Home décor made about 34.40% of the of total sales, with about $8,870,000 Revenue from 17,000 quantity sold, revenue generated is consistence across the quarters with minimal difference
2.	Clothing of 33.90% of total sales with revenue of $7,660,000 from 17,000 quantity sold, revenue generated is at high at 2nd (spring)  and 3rdquarter (Autumn) of the year
3.	Electronics which make the least percentage of the total sales 31.70% with revenue of $8,380,00 from 16,000 quantity sold, revenue is high at the 1st (winter) and 3rd quarters (Autumn)

## 3.Top most valuable customers
- 	Out of 10 most valuable customers, 3 are high valued customer and the rest are returning customers, which are likely to churn
![Screenshot 2025-03-14 154408](https://github.com/user-attachments/assets/acf3f7b5-4077-4061-83b9-43754505b741)

## **4. Monthly Sales Trends**
- values are evenly distributed across the month in term of total quantity sold 
-	Peak sales occurred in November and December (due to holiday promotions), January and increase begins in February.
-	Slowest sales were recorded in November and January with about 3,500 quantities of orders.
-	Highest sales were recorded in June with almost 5,000 quantities of orders

## **5. customer segmentation**
-	Customers with just 1 order are classify as new customer, customers with orders greater than 1 but less than 5 are classify as Returning customers, and customers with orders of 5 and above are classify as High value customers 
-	Total quantity of orders by new customers is 17,148 which is 34.18% of the total quantity sold, Total quantity of orders by returning customers is 31,035 which is 61.85% of the total quantity sold and high valued customers made just 3.97% of 1,992 quantities 
-	The Average product order by new customer is 48.85 products, returning customer of 50.55 products and high value customer is 56.91 products
-	The rate at which customers churn in relation with customer segment, returning customers 27.71% churn rate suggests that a significant portion of returning customer will be leaving or not making repeat purchases while the 72.29% of customers who are classified as high-value have low or no churn, meaning they are more likely to stay and continue spending. 

## **6. Revenue by state**
-	China and Indonesia have the highest revenue 
-	Thailand, Poland and Sweden have same revenue generated and they have the least
![Screenshot 2025-03-14 154537](https://github.com/user-attachments/assets/3918a7c9-0440-4abe-9466-484c09e47498)

## **7. Yearly growth**
-	Yearly growth rate from 2020 to 2021 is 4.08% with change in revenue from $8,010,000 to $8,340,000
-	Yearly growth rate from 2021 to 2022 is 2.53%, with change in revenue from $8,340,000 to $8,550,000
The growth rate across the years is positive but low
![Screenshot 2025-03-14 164254](https://github.com/user-attachments/assets/f0eb7228-0cf1-4227-892d-b3f8dcb2e546)
- [To view power bi dashboard page 1 click here](https://ibb.co/KpWy1X2S)
- [To view power bi dashboard page 2 click here](https://ibb.co/dwjH9vFg)

## **8.Conclusion and Recommendations**
-	There is positive growth grate across the year but its low 
-	China and Indonesia generated the most revenue compare to other country
-	There is no significant difference across the year, but sales are affected during holiday periods
-	Returning customers are likely to churn due to unsatisfaction

## **Recommendations**
-	Offering discounts to low-spending customers
-	Implementing loyalty rewards for frequent shoppers
-	Set a special recognition gift for high valued customers
-	Increase advert during holidays and festive periods
-	Create a friendly survey for customers to know how to serve them better 










