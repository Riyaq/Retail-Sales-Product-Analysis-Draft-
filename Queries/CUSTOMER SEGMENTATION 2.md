## 9. What is the age distribution of customers who shop regularly?
In analytics, regular shoppers usually means customers who purchased more than a threshold (e.g., X transactions in a given period).
<br>
For simplicity, let’s define:<br>
👉 A regular customer = someone with at least 3 transactions in the dataset.
<br>
<br>
<br>
Create two Calulated column in Customers table [ Go to Report view > Click on 3 dot > New Column ]<br>
```
Age(Calculated Column) = DATEDIFF(Customers[birthdate], TODAY(), YEAR)
```
```
Age Group (Calculated Column) = 
IF(Customers[Age] < 25, "18-24",
    IF(Customers[Age] < 35, "25-34",
        IF(Customers[Age] < 45, "35-44",
            IF(Customers[Age] < 55, "45-54",
                "55+"
            )
        )
    )
)
```
Create one Measure - <br>
```
Regular Customers (Measure) = 
CALCULATE(
    DISTINCTCOUNT(Customers[customer_id]),
    FILTER(
        Customers,
        CALCULATE(COUNTROWS(Transactions)) > 3

    )
)
```
<img width="596" height="136" alt="lCapture" src="https://github.com/user-attachments/assets/87d3b919-9fdf-4393-a56a-0d636d472359" />
