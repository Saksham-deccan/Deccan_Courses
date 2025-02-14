## <span style="color:#364BC9"> Nautral Language Query </span>
Which part had the largest increase in the number of orders from 1993 to 1994?

## <span style="color:#364BC9"> SQL Query </span>

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
### Let's try to understand why this NLQ & SQL pair is good through the video below:

<iframe src="${PRIVATE_NLQ_SQL_PAIR_2}"
        width="800"
        height="450"
        frameborder="0"
        allowfullscreen>
</iframe>