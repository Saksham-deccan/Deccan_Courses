## <span style="color:#364BC9"> Nautral Language Query </span>
What is the difference in the average order price for customers from the BUILDING and MACHINERY market segments?

## <span style="color:#364BC9"> SQL Query </span>

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

### Let's try to understand why this NLQ & SQL pair is good through the video below:

<iframe src="${PRIVATE_NLQ_SQL_PAIR_1}"
        width="800"
        height="450"
        frameborder="0"
        allowfullscreen>
</iframe>