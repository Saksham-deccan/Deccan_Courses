## Nautral Language Query
What is the difference in the average order price for customers from the BUILDING and MACHINERY market segments?

## SQL Query

```
SELECT 
    ABS(
        AVG(CASE 
                WHEN c.c_mktsegment = 'BUILDING' THEN o.o_totalprice 
            END) 
        - 
        AVG(CASE 
                WHEN c.c_mktsegment = 'MACHINERY' THEN o.o_totalprice 
            END)
    ) AS diff_in_avg_order_price
FROM orders AS o
LEFT JOIN customer AS c 
    ON c.c_custkey = o.o_custkey
WHERE c.c_mktsegment IN ('BUILDING', 'MACHINERY');


```