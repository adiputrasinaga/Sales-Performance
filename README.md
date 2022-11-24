<u><h3>Sales-Performance</h3></u>
<br/>


The dataset used contains transactions from 2009 to 2012 with a total of 5500 raw data, including order status which is divided into finished orders, returned orders and canceled orders.

The dataset that has been provided and will be used in this project contains the following data.
OrderID
Order Status
Customer
Order Date
Order Quantity
Sales
Discount %
Discount
Product Category
Product Sub-Category

The table name that will be used in this project is dqlab_sales_store

**Overall Performance by Year**

Query using SQL to get total sales (sales) and number of orders (number_of_order) from 2009 to 2012 (years).

````sql
SELECT year(order_date) as years, sum(sales) as sales, COUNT(*) as number_of_order
FROM dqlab_sales_store
WHERE order_status = 'Order Finished'
GROUP BY years
````
