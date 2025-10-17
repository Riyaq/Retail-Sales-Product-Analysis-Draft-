## 2. How does purchasing behavior differ by marital status or gender?
The company wants to know which customer segments (by gender, marital status, or yearly income) contribute most to sales

https://github.com/Riyaq/Retail-Sales-Product-Analysis/blob/main/DAX%20Queries%20for%20Analysis.md
<br>
<img width="632" height="326" alt="Capturooe" src="https://github.com/user-attachments/assets/09d20a23-ac0c-4da5-b47f-0b6a587223d4" />
<br>
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
