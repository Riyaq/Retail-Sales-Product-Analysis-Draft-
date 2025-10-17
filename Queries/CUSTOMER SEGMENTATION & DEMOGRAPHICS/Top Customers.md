## Find top customers by total purchase value?

Aggregate by customer_id, join Transactions, calculate revenue

```
Top 3 Customers by Sales = 
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
