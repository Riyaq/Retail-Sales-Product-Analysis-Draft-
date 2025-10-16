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
<br>
<img width="632" height="326" alt="Capturooe" src="https://github.com/user-attachments/assets/09d20a23-ac0c-4da5-b47f-0b6a587223d4" />
**Gender-Based Purchasing Behavior**
<br>
Bar Chart: <br>
X-axis: Customers[Gender]
Y-axis: [Total Sales]
Tooltip: [Average Order Value], [Purchase Frequency]
<br>
Donut Chart: <br>
Values: [Total Sales]
Legend: Customers[Gender]
<br>

**Marital Status Analysis**
<br>
Clustered Column Chart:
X-axis: Customers[Marital_Status]
Y-axis: [Total Sales]
Legend: Customers[Gender]
Tooltip: [Average Order Value], [Purchase Frequency]
<br>
Table / Matrix:
Rows: Customers[Marital_Status]
Columns: Customers[Gender]
Values: [Total Sales], [Total Profit], [Purchase Frequency]


## 3. What’s the average revenue generated per customer segment (income, education, region)?
```
AVG order value = 
DIVIDE(
    [Total Sales],
    COUNTROWS(Transactions))

AVG revenue per Customer = 
DIVIDE( [Total Sales],
DISTINCTCOUNT(Transactions[customer_id]))
```
**Avg Revenue by Education**

Table <br>
Rows: Customers[education]
<br>
Values: [Avg Revenue per Customer]
<br>

**Avg Revenue by Region**
Bar Chart - Y - Sales_region, X - AVG order Value, Tool tip- AVG revenue per Customer.
<br>
This Slicer will work.



<img width="970" height="457" alt="Captuure" src="https://github.com/user-attachments/assets/5d171a06-bc43-44be-9788-60d0bcb4b620" />





<img width="924" height="436" alt="Captuhhre" src="https://github.com/user-attachments/assets/112d6775-1771-4278-a549-d19fe49f436c" />



