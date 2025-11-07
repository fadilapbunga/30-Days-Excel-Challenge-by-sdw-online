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

- First, to make it easier to use pivot tables, convert the table in __Enrollment Data__ sheet into a table named __‘table’.__ This makes it easier when it is asked to enter the data table to be pivoted by simply writing the table name.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/72c39a1c-dd49-4177-9d71-29ac98920489" />

- Drag __Region__ field to __Rows__ and drag __Monthly Payment ($)__ to __Values__.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/aa9dcc07-1514-48ee-b356-333c8befc40b" />

---

✅ __Task 2: Most Popular Subscription Type__
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/1ee590a1-2de2-4e7a-a782-7c674809112a" />

---

✅ __Task 3: Most Common Signup Channel__
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/f203d20c-67bc-4a2b-a5ed-d76c441c3c13" />

---

✅ __Task 4: Most Engaged Age Group__
<img width="1920" height="1021" alt="image" src="https://github.com/user-attachments/assets/5ef1bf00-0073-4af5-9e09-1f0cd9dacc11" />

---

✅ __Task 5: Where are Pro Students Enrolled?__
<img width="1920" height="1021" alt="image" src="https://github.com/user-attachments/assets/d2b47e44-4f37-4591-beed-8036089d4d7c" />

---

📌 __BONUS__








***

### <div align="center">Results Overview</ins></div>
