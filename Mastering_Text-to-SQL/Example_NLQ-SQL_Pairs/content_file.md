# Example\_1

:::tip
What is the difference in the average order price for customers from the BUILDING and MACHINERY market segments?
:::

```txt
SELECT ABS(AVG(CASE WHEN c.c_mktsegment = 'BUILDING' THEN o.o_totalprice END) - AVG(CASE WHEN c.c_mktsegment = 'MACHINERY' THEN o.o_totalprice END)) AS diff_in_avg_order_price
 FROM orders AS o
 LEFT JOIN customer AS c ON c.c_custkey = o.o_custkey
 WHERE c.c_mktsegment IN ('BUILDING', 'MACHINERY')
```

# Example\_2

:::tip
Which part had the largest increase in the number of orders from 1993 to 1994?
:::

```txt
WITH order_date_1993 AS (
 SELECT lineitem.l_orderkey,lineitem.l_partkey,orders.o_orderdate
 FROM lineitem
 JOIN orders ON lineitem.l_orderkey = orders.o_orderkey
 WHERE strftime('%y',orders.o_orderdate) = 1993
 )
 , order_date_1994 AS (
 SELECT lineitem.l_orderkey,lineitem.l_partkey,orders.o_orderdate
 FROM lineitem
 JOIN orders ON lineitem.l_orderkey = orders.o_orderkey
 WHERE strftime('%y',orders.o_orderdate) = 1994
 )
SELECT part.p_name
FROM order_date_1994
LEFT JOIN part ON order_date_1994.l_partkey = part.p_partkey
LEFT JOIN order_date_1993 ON order_date_1993.l_partkey = part.p_partkey
GROUP BY part.p_name
ORDER BY (count(order_date_1994.l_partkey) - count(order_date_1993.l_partkey))  DESC
LIMIT 1
```