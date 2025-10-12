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

## 2. How does purchasing behavior differ by marital status or gender?
The company wants to know which customer segments (by gender, marital status, or yearly income) contribute most to sales

https://github.com/Riyaq/Retail-Sales-Product-Analysis/blob/main/DAX%20Queries%20for%20Analysis.md
<img width="632" height="326" alt="Capturooe" src="https://github.com/user-attachments/assets/09d20a23-ac0c-4da5-b47f-0b6a587223d4" />






