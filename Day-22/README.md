# 2️⃣2️⃣ Day 20: Data visualization – part 2 (Advanced charts)

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

### <div align="center">Identification Database</ins></div>
You're working as a Junior Data Analyst for a UK-based public health initiative.
You’ve been given data from a recent campaign and need to create visuals that tell a story.

✅ __Dataset 1 (Sheet: campaign_engagement):__
- 'campaign_engagement' → Summary by city
- Fields: City, Reach, Registrations, Completion Rate (%)

<div align="center"><img width="743" height="241" alt="image" src="https://github.com/user-attachments/assets/d19e1914-2adc-4047-b45e-36a1c789af03" /></ins></div>  

✅ __Dataset 2 (Sheet: audience_by_age):__
- 'audience_by_age' → Engagement breakdown by age group
- Fields: Age Group, Registrations, Completion Rate (%)

<div align="center"><img width="525" height="245" alt="image" src="https://github.com/user-attachments/assets/2dcd88e6-0721-4b9c-a2ee-52419621469a" /></ins></div>  

✅ __Dataset 3 (Sheet: droupout_analysis):__
- 'dropout_analysis' → People who registered vs completed appointments
- Fields: City, Registered, Completed, Dropouts, Dropout Rate (%)

<div align="center"><img width="631" height="251" alt="image" src="https://github.com/user-attachments/assets/c72b34a2-991c-4ba4-815f-e00024159077" /></ins></div>  

***

### <div align="center">Identification Issues</ins></div>
📌 __Scenario:__  
The campaign ran across 6 UK cities to raise awareness around mental wellbeing and access to free health checkups.
You need to build visuals that help your managers and stakeholders answer these questions:
- Which cities are seeing the highest campaign reach?
- Are people completing their appointments after registering?
- Which age groups are engaging most with the campaign?
- Are there any red flags we should be aware of?

🛠️ __Tasks:__  
1️⃣ Use bar charts to compare city-level engagement.  
2️⃣ Use colour intentionally to highlight trends or outliers.  
3️⃣ Sort your data so high-performing categories are easier to spot.  
4️⃣ Remove gridlines and clutter to keep visuals clean.  
5️⃣ Add clear chart titles and subtitles to tell the story behind the numbers.

***

### <div align="center">Solving Step or Analysis</ins></div>
1️⃣ __Which cities are seeing the highest campaign reach?__  
- To find out which cities achieved the highest campaign engagement, this can be found in the __campaign_engagement sheet__, select the __City__ and __Reach__ columns, and create a bar chart to see the results.
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/d0d346f6-ceaf-4e0c-871d-d2d1197fa3d1" /></ins></div>

ganti judul dan tebalkan
hilangankan gridlines
hilangkan vertical value
tambahkan data labels di Inside End, ubah tulisan menjadi putih, begitupun dengan Horizontal (Category) Axis
ubah Gap Width pada series 'Reach' menjadi 60% sehingga tampilan bar dari satu kota kekota lain terlihat tidak terlalu berjarak dan lebih tebal

---
2️⃣ __Are people completing their appointments after registering?__
- To find out whether people completed their appointments after registering, how many completed and how many dropped out, this can be found in the __dropout_analysis sheet.__
- First, use a pivot table to sum up each of these. The __Pivot Field__ contains the __‘Completed’ and ‘Dropout’__ columns, which are dragged to __Values__ in __SUM__ format and given the title __‘Yes’__ for people who completed and __‘No’__ for people who did not complete.
<div align="center"><img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/5a3c8242-8514-45ee-9b70-3caad4056c36" /></ins></div>

---
3️⃣ __Which age groups are engaging most with the campaign?__
- To find out which age groups are most actively participating in this campaign, it can be seen in the audience_by_age data sheet, select the __Age Group__ and __Registration__ columns, and create a column chart to see the results.
<div align="center"><img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/62a62d70-804b-4713-b1e3-6389d831b33c" /></ins></div>

---
4️⃣ __Are there any red flags we should be aware of?__

- Yes, first on the __campaign_engagement sheet__, the __Completion Rate__ column shows the __wrong percentage__ value for the reach rate of each city.
- So, to calculate the campaign reach rate for each city, create a __new column__ named __‘Reach Rate’__ with the following formula:
````excel
        =($C2/$B2)*100
 ````
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/6a70d5a1-4971-42ef-828c-ad7b3e07ecfa" /></ins></div>

---

- The second error is in the __audience_by_age__ sheet, where several inaccuracies were found. The first is that when adding up the total number of registered participants, the total is 5,700, whereas the number of registered participants when viewed from the other two sheets is 11,500.
<div align="center"><img width="1608" height="638" alt="image" src="https://github.com/user-attachments/assets/0452c1ec-b441-4b02-80f1-14db0c3ef797" /></ins></div>

- The second error found is that the __Completion Rate on the audience_by_age sheet__ cannot be considered valid because it is not fundamental. We cannot calculate the completion rate because there is no calculation division that can be done there. However, keep in mind that sometimes some data is just as it is when we receive it, and it can still be used for analysis if needed in general terms.

---
- Additionally, on the dropout_analysis sheet, add a new column to complete the data in the analysis, namely the __Completion Rate (%)__ column, which is __the inverse of the Dropout Rate (%) column__, using the formula:
````excel
        =($C2/$B2)*100
 ````
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/bf28b611-db93-4d2e-acec-ef23e2084a76" /></ins></div>

***

### <div align="center">Results Overview</ins></div>

<div align="center"><img width="1009" height="555" alt="image" src="https://github.com/user-attachments/assets/58932f55-7fe7-4748-bc54-69c0777b4645" /></ins></div>

