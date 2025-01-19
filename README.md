# Maven_Pizza_Challenge
Maven challenge with Pizza Sales dataset
https://mavenanalytics.io/data-playground?order=date_added%2Cdesc&search=pizza

Pizza Place Sales
A year's worth of sales from a fictitious pizza place, including the date and time of each order and the pizzas served, with additional details on the type, size, quantity, price, and ingredients.

Recommended Analysis
How many customers do we have each day? Are there any peak hours?

How many pizzas are typically in an order? Do we have any bestsellers?

How much money did we make this year? Can we indentify any seasonality in the sales?

Are there any pizzas we should take of the menu, or any promotions we could leverage?

DAX used:
Total Revenue = SUMX('pizzas','pizzas'[price] * [Total Orders])
Total Pizza sold = SUMX(order_details,order_details[quantity]* [Total Orders])
Total Orders = COUNTROWS(order_details)
Each Pizza Count = COUNTX(order_details,order_details[pizza_type_id])
