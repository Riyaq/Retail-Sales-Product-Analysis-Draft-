## 10. Do homeowners purchase differently than renters?
Compare homeowner = 'Y' vs. 'N'
<br>
```
Total Sales = SUMX(Transactions, Transactions[Quantity] * RELATED(Products[product_retail_price]))

AVG order value = DIVIDE( [Total Sales], COUNTROWS(Transactions))

Purchase Frequency = DIVIDE(COUNTROWS(Transactions), DISTINCTCOUNT(Customers[customer_id]))

AVG revenue per Customer = 
DIVIDE( [Total Sales],
DISTINCTCOUNT(Transactions[customer_id]))
```
