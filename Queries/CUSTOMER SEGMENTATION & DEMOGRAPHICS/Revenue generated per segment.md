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
