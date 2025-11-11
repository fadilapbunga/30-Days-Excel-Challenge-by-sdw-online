# 1️⃣1️⃣ Day 11: Pivot tables – part 1

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

### <div align="center">Identification Database</ins></div>
There is enrollment data sheet from online learning platfrom, we were asked to help analyze student behavior. There are: __Student ID, Region,	Course Name,	Subscription Type,	Signup Channel,	Age Group,	Monthly Payment ($),	Videos Watched (Month) columns.__
<div align="center"><img width="960" height="509" alt="image" src="https://github.com/user-attachments/assets/12cbec33-96fb-4fec-ba91-0543bd1bc340" /></ins></div>

***

### <div align="center">Identification Issues</ins></div>
Use Pivot Tables to explore engagement, revenue, and sign-up performance.

✅ __Task 1: Revenue by Region__
- Rows → Region
- Values → Sum of Monthly Payment ($)
- Sort from highest to lowest

✅ __Task 2: Most Popular Subscription Type__
- Rows → Subscription Type
- Values → Count of Student ID

✅ __Task 3: Most Common Signup Channel__
- Rows → Signup Channel
- Values → Count of Student ID

✅ __Task 4: Most Engaged Age Group__
- Rows → Age Group
- Values → Sum of Videos Watched (Month)

✅ __Task 5: Where are Pro Students Enrolled?__
- Rows → Course Name
- Columns → Subscription Type
- Values → Count of Student ID
- Filter for only 'Pro'

📌 __BONUS__
Use slicers or pivot charts to enhance your analysis.

***

### <div align="center">Solving Step or Analysis</ins></div>
✅ __Task 1: Revenue by Region__

- First, to make it easier to use pivot tables, convert the table in __Enrollment Data__ sheet into a table named __‘table’.__ This makes it easier when it is asked to enter the data table to be pivoted by simply writing the table name. And select the pivot table area in the new sheet that has been created, named __Pivot Table__ in __B3__.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/72c39a1c-dd49-4177-9d71-29ac98920489" />

---

- Drag __Region__ field to __Rows__ and drag __Monthly Payment ($)__ to __Values__.
- Sort from highest to lowest
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/aa9dcc07-1514-48ee-b356-333c8befc40b" />

***

✅ __Task 2: Most Popular Subscription Type__

- Create a new pivot table area in __E3__.
- Drag __Subscription Type__ field to __Rows__ and drag __Count of Student ID__ to __Values__.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/1ee590a1-2de2-4e7a-a782-7c674809112a" />

***

✅ __Task 3: Most Common Signup Channel__

- Create a new pivot table area in __B12__.
- Drag __Signup Channel__ field to __Rows__ and drag __Count of Student ID__ to __Values__.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/f203d20c-67bc-4a2b-a5ed-d76c441c3c13" />

***

✅ __Task 4: Most Engaged Age Group__

- Create a new pivot table area in __E12__.
- Drag __Age Group__ field to __Rows__ and drag __Sum of Videos Watched (Month)__ to __Values__.
<img width="1920" height="1021" alt="image" src="https://github.com/user-attachments/assets/5ef1bf00-0073-4af5-9e09-1f0cd9dacc11" />

***

✅ __Task 5: Where are Pro Students Enrolled?__

- Create a new pivot table area in __I3__.
- Drag __Course Name__ field to __Rows__, drag __Subscription Type__ field to __Columns__, and drag __Count of Student ID__ to __Values__.
- Filter for only 'Pro'
<img width="1920" height="1021" alt="image" src="https://github.com/user-attachments/assets/d2b47e44-4f37-4591-beed-8036089d4d7c" />

***

📌 __BONUS__

- To do slicer on pivot table, click __PivotTable Analyze__ tab and __Insert Slicer__. Check the column to be selected. Here, try to check the __Region__. And add __Bar Chart__ region field by click __Pivot Chart__.
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/b66acae0-90cc-4ed5-9672-decb2b854310" />

---

- Make sure that __Report Connections__ for __Region__ is into __PivotTable 1__ as we created before. But for some analyze it can be change based on the purpose. But here, i try to only connect into one pivot table.
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/5e80dc1b-2a88-45d2-8a1e-3b8e5858c97b" />

---

- In the __slicer__, we can choose whether we want to display regions in several areas or all of them. Below, I tried to display only regions from Africa and Asia, so I only needed to click on those regions and the chart would follow.
<img width="1920" height="1021" alt="image" src="https://github.com/user-attachments/assets/a0c9bb18-b2ef-4967-a134-fbbe05172222" />

---

- For another, i tried to display only regions from Africa and the chart only showed data from Africa.
<img width="1920" height="1021" alt="image" src="https://github.com/user-attachments/assets/45d53d65-41de-4627-83e3-1fe729ea164c" />

---

- In the slicer, you can also combine charts between pivot table 1 and other pivot tables. Below are images of each chart from each pivot table that has been created above. And each has its own slicer on the right. 
<img width="960" height="510" alt="image" src="https://github.com/user-attachments/assets/c877db6e-8943-4a58-a2b9-89cc7999611f" />

- When collecting data, for example, we want to know how the Online Course Enrollment Tracker from North America and South America is performing among people aged 25-34. The chart will display this information, allowing us to carefully examine the data. We can see that people from North America and South America are not taking Python courses with a free subscription, and they are not taking SQL Mastery courses with a pro or standard subscription. And most of them sign up through Email Campaigns.
<img width="1920" height="1017" alt="image" src="https://github.com/user-attachments/assets/494fb058-cff9-4b2c-9652-50e838d6f8f5" />

***

### <div align="center">Results Overview</ins></div>
