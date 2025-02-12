## Nautral Language Query
Which part had the largest increase in the number of orders from 1993 to 1994?

## SQL Query

```
WITH order_date_1993 AS (
    SELECT 
        lineitem.l_orderkey, 
        lineitem.l_partkey, 
        orders.o_orderdate
    FROM lineitem
    JOIN orders 
        ON lineitem.l_orderkey = orders.o_orderkey
    WHERE strftime('%Y', orders.o_orderdate) = '1993'
), 
order_date_1994 AS (
    SELECT 
        lineitem.l_orderkey, 
        lineitem.l_partkey, 
        orders.o_orderdate
    FROM lineitem
    JOIN orders 
        ON lineitem.l_orderkey = orders.o_orderkey
    WHERE strftime('%Y', orders.o_orderdate) = '1994'
)

SELECT 
    part.p_name
FROM order_date_1994
LEFT JOIN part 
    ON order_date_1994.l_partkey = part.p_partkey
LEFT JOIN order_date_1993 
    ON order_date_1993.l_partkey = part.p_partkey
GROUP BY part.p_name
ORDER BY 
    (COUNT(order_date_1994.l_partkey) - COUNT(order_date_1993.l_partkey)) DESC
LIMIT 1;



```