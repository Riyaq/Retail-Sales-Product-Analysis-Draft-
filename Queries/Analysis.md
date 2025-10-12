## 1. Find out TOP 3 customer by sales
```
Top 5 Customers by Sales = 
CALCULATE (
    [Total Sales],
    KEEPFILTERS(TOPN (
        3,
        ALL( 'Customers'[customer_id] ),
        [Total Sales],
        DESC
    )
 )
)
```
