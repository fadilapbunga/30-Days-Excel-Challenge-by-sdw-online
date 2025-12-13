# 2️⃣1️⃣ Day 21: Practice (Week 3 review)

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

### <div align="center">Identification Database</ins></div>
🧠 __Scenario: UK Tech Conference Post-Event Feedback__

You've been given feedback data from a recent UK tech event series held in multiple cities.
Your job is to clean and prep this for insights using Power Query + PivotTables.

🧾 __Sheet: 'Event_Feedback_Responses' (~1500 records)__
<div align="center"><img width="1569" height="577" alt="image" src="https://github.com/user-attachments/assets/1f5985e4-abad-4d0f-92bc-fe982391df75" /></ins></div>

***

### <div align="center">Identification Issues</ins></div>
✅ __TASKS TO COMPLETE__

1️⃣ Load the data into Power Query  
2️⃣ Standardize 'Event Track' and 'Session Type' to Proper Case  
3️⃣ Remove exact duplicates (based on all columns)  
4️⃣ Filter out blank Satisfaction scores  
5️⃣ Replace missing 'Experience Rating' with average rating per Event Track  
6️⃣ Add a new column to categorize ratings:
   - 8–10 = 'Excellent', 5–7 = 'Okay', 1–4 = 'Poor'

7️⃣ Add a 'Feedback Length' column to count the number of words  
8️⃣ Load cleaned table back into Excel

📈 __PIVOT TABLE CHALLENGE:__

1️⃣ Count feedback entries by City and Session Type  
2️⃣ Average rating by Event Track

📊 __DASHBOARD IDEAS (Optional):__
- Slicer for City
- Bar chart showing average satisfaction per track
- Timeline of submissions per week

***

### <div align="center">Solving Step or Analysis</ins></div>
1️⃣ 

To load data into Power Query, you can do the following:  
__Data ▶️ Get Data ▶️ From Other Sources ▶️ From Table/Range__
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/31ea38eb-084e-4f0d-abd1-3664e16495a5" /></ins></div>

---
2️⃣

To ensure that there are no extra spaces in the data, you can use trim. Here, the columns to be checked are the ‘Event Track’ and ‘Session Type’ columns, so the steps to be taken are:  
__Block the ‘Event Track’ and ‘Session Type’ columns ▶️ Transform ▶️ Format ▶️ Trim__
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/49a41c59-5bb1-433e-87f5-8b76b6a5437c" /></ins></div>

---
3️⃣

Ensure that there is no duplicate data in all columns by:  
__Selecting all columns ▶️ Home ▶️ Remove Rows ▶️ Remove Duplicates__
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/e14a036a-110d-4921-9965-83dfe0537043" /></ins></div>

---
4️⃣

To filter out satisfaction scores, or only display data that is not blank/null, simply can __click the small arrow to the right of the satisfaction column__ and __select Remove Empty__.
<div align="center"><img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/b4e1181e-e515-44c3-81bc-37a151ccfb33" /></ins></div>

---
5️⃣  
To replace the missing __‘Experience Rating’__ with the __average rating per Event Track__, one of the steps that can be taken is to combine __Group By__ and __Merge Query__. On another occasion, another way to do this is to use the __IF formula__. However, on this occasion, I want to use the method of combining __Group By and Merge__.

---

- First, we __duplicate__ the query to create a group by the average experience rating based on Event Track, then we change the query name to __'Group By Avg'__.
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/a9a7c810-8197-4ec4-827b-c8014e735ecd" /></ins></div>
<div align="center"><img width="276" height="400" alt="image" src="https://github.com/user-attachments/assets/f9c44eb4-6601-4dac-97fe-815cee1946bd" /></ins></div>

---

- Then, in the __‘Group By Avg’__ query, click the __Event Track__ column and click __Group By__ on __Home__. Give the newest column the name __‘avg_ratings’__ with the __Average__ operation on __Experience Ratings__.
<div align="center"><img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/fb7eab46-63ff-44d7-9520-61c183aec389" /></ins></div>

---

- Then round the average to one decimal place by going to __Add Column ▶️ Round ▶️ and typing 1.__
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/7c204f2c-814d-40f5-99eb-353a383ef93e" /></ins></div>

---

- Then merge the two queries with a __Left Outer Join__, which keeps all the rows from __the left table (Table 1)__ and brings in any matching rows from __the right table (Group By Avg)__.
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/cc01860c-b995-4f30-9768-cda191478f7c" /></ins></div>

---

- The merge was successful. __Expand the table results (displaying the average numbers)__ by clicking __the two arrows__ in the Group By Avg column and clicking __Round__.
<div align="center"><img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/8c737edd-7434-4f0a-b9d1-6a613a42f395" /></ins></div>

---

- Then, the next step is to create a new column titled __Experience Rating_New__, where the null data should already contain average data based on Event Track with the formula below:
````excel
      = if [Experience Rating] = null
      then [Group By Avg.Round]
      else [Experience Rating]
 ````

<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/a08e39e4-5ccc-4ce3-b9a6-c0590c06c7b2" /></ins></div>

---
6️⃣

- Create a __Rating Categorize__ by adding a Conditional Column, where ratings >= 8 are labeled __“Excellent”__, ratings >= 5 are labeled __“Okay”__, and all others are labeled __“Poor”__, as shown in the image below.
<div align="center"><img width="1920" height="1022" alt="image" src="https://github.com/user-attachments/assets/39e8fe1d-329f-435a-8b9b-8c06553d8efa" /></ins></div>

---
7️⃣

- Create a new column called __Feedback Length__, which is the number of characters in the feedback. The formula is as follows:
````excel
    = if ([Feedback]= null) then ""
      else Text.Length ([Feedback])
 ````

<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/da3d4d1c-8c5d-4bae-90cc-6c59e827aad9" /></ins></div>

---

- As an addition to data cleaning, here I want to change the data in the __Submitted On__ column to __only the Date format__, not the Date and time. To change this, click the small arrow next to the column and then click __Date__.
<div align="center"><img width="1920" height="1016" alt="image" src="https://github.com/user-attachments/assets/e39bf48a-73a1-440e-8b83-91818cb88fc1" /></ins></div>

---

📈 __PIVOT TABLE CHALLENGE:__

1️⃣ Counting feedback entries based on City and Session Type with a pivot table is done as follows:

- Drag __City__ field to __Rows__, drag __Session Type__ to __Columns__, and drag __Count of Feedback__ to __Columns__
<div align="center"><img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/81542105-d80a-4119-8a20-f790acce492c" /></ins></div>

---

2️⃣ Average rating by Event Track with a pivot table is done as follows:

- Drag __Event Track__ field to __Rows__ and drag __Average Experience Rating__ to __Values__.
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/9299301f-1f43-46df-8044-a45d469debab" /></ins></div>

---

📊 __DASHBOARD IDEAS (Optional):__


***

### <div align="center">Results Overview</ins></div>
