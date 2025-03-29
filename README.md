# Indian Traffic Violations and Statistics Dashboard
Dashboard Link : https://app.powerbi.com/links/TbwoA47iqg?ctid=7ce3ab11-7ef4-4221-8058-97761f65b97e&pbi_source=linkShare

Note : If the link is not working view the powerbi files in repository.
## Problem Statement
**Problem Statement:**  
The dataset contains 4,000 records with 33 columns detailing traffic violations, including information on violation types, fines, driver demographics, vehicle data, environmental conditions, safety compliance, and enforcement actions. The goal is to analyze this data to:

1. **Identify Patterns and Trends**: Understand the frequency and types of violations, demographic behaviors, and geographical distribution.
2. **Evaluate Safety Compliance**: Measure adherence to safety regulations such as helmet usage, seatbelt compliance, and speed limits.
3. **Assess Enforcement Effectiveness**: Determine the role of license validity, penalty points, and court appearances in reducing violations.
4. **Develop Actionable Insights**: Provide recommendations to improve traffic safety, compliance, and enforcement mechanisms.
---

The insights derived from this analysis could inform policy decisions, enhance driver education programs, and optimize enforcement strategies to reduce traffic violations and improve road safety.

---
Dashboard
-
![Image](https://github.com/user-attachments/assets/0b59e9c7-cf85-432d-aedf-835c8afb1e72)
-
* The above Dashboard contains various visualizations that helps in gaining insights on how indian traffic violatons are monitored by the system.
---
**Steps** :

1. Collecting of data from kaggel
2. Cleaning the raw data in power bi by transforming it.
3. Creating new measures for easy manipulation of the datasets.
4. Removing null values and empty or blank cells in the data.
5. Adding visual charts.
---
**Min, Max, Total**

The image contains minimum fine amount, and the maximum fine amount, along with total number of violations and the total fine amount collected.

* Card is used as a visual representation

![Image](https://github.com/user-attachments/assets/6c2fbb3e-a753-4fd4-a62c-456ca984dc35)

---
**Locations**

The visualization used is a **tree map** it has all the states present in the data and the total violations in each states.

![Image](https://github.com/user-attachments/assets/ef87a7dc-1b15-48b2-adc1-7c629db8cc64)

---
**Violations by year and month**

It shows the number of violations took place by each year and months, along with the total fine collected in each time line.

* line chart is used for this representation

![Image](https://github.com/user-attachments/assets/6d620d2a-ab75-4667-900d-c7694b442eac)

---
**vehicle types**

For this a **Slicer** is used to represent the types of vehicles in the data, which can give more precise and accurate insights for each vehicle types.

![Image](https://github.com/user-attachments/assets/14600c26-0823-4771-9c2c-097260306b17)

---
**Violations and license validity**

It shows the previous violations data along with total violation for differnt type of license validity category in form of **Line Chart**.

![Image](https://github.com/user-attachments/assets/5aa3c7a9-5e3f-45eb-9b4c-28d20a3758b7)

---
**Types of Violations**

It shows the total number of violations by each violation category for this a **Bar chart** is used.

![Image](https://github.com/user-attachments/assets/8c9c9045-c4b1-4977-96c3-84f33e492555)

---
**Violations by gender**

Shows the total violations by each gender a **column chart** is used for representation.

![Image](https://github.com/user-attachments/assets/39698137-54e5-4afa-b575-3bf636e69b68)

---
**People required to appear for court**

Shows the total percentage and total number people required to appear for court with category as legends, a **Pie chart** is used for representation.

![Image](https://github.com/user-attachments/assets/78b31935-188d-48bf-a252-3f0c0ac67dd3)

---
**Fine paid by people**

Shows the total percentage and the total number of fine paid by people, **pie chart** is used to represent.

![Image](https://github.com/user-attachments/assets/0ebdedc4-a6bc-4ef9-8df2-e21ce899b834)

---
**speed compliance percentage**

Shows the average speed compliance with minimum and maximum percentage, a **guage chart** is used for representation, and a new measure is created for this calculation.

```http

Speed_Compliance_Percentage = DIVIDE(
    COUNTROWS(FILTER(Indian_Traffic_Violations, Indian_Traffic_Violations[Recorded_Speed] <= Indian_Traffic_Violations[Speed_Limit])),
    COUNTROWS(Indian_Traffic_Violations)
) * 100
```
* This measure calculates the percentage of drivers who adhered to speed limits in dataset. It filters the data to include only rows where the recorded speed is less than or equal to the speed limit, counts these compliant records, and divides this count by the total number of records in the table. The result, expressed as a percentage, provides a clear metric for understanding speed compliance among drivers.

![Image](https://github.com/user-attachments/assets/399fc850-3885-447c-8df2-ba46e53b5ab0)
---
**Payment Methods**

Shows how many people are using differnt payment methods, along with percentage of each category and the total users of each category, a **donut chart** is used for representing the stats.

![Image](https://github.com/user-attachments/assets/9b7bea61-8766-46b1-8132-54846f181eb6)

---
**Data source** :
kaggel

**Tool used** : Power bi

**Readme file** : readme.so

**linkedin profile** : www.linkedin.com/in/charan-r-b04875358
