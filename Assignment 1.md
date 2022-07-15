# Assignment 1
## Q1.



## Q2. JOIN Tables
SQL Syntax:
~~~SQL

SELECT 
o.order_id,
o.user_id,
o.order_number,
o.order_dow,
o.order_hour_of_day,
o.days_since_prior_order,
op.product_id,
op.add_to_cart_order,
op.reordered,
o.eval_set
FROM "orders" o
INNER JOIN "order_products" op 
ON o.order_id = op.order_id
WHERE o.eval_set = 'prior'
LIMIT 10;
