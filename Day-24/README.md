# 2️⃣4️⃣ Day 24: Power Query – part 2

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

### <div align="center">Identification Database</ins></div>
🎯 __Scenario:__  
You work for UrbanKart's central analytics team.  
Your goal is to consolidate and clean the sales data from multiple city branches and vendors to generate insights and prepare for a monthly performance review.

---
✅ __Sheet: Sales_Data__  
Columns include: Transaction ID,	Date,	City,	Customer Name,	Product,	Units Sold,	Unit Price,	Payment Method, and	Total Revenue.  
<div align="center"><img width="1559" height="571" alt="image" src="https://github.com/user-attachments/assets/9d14d083-2c02-442f-877f-74620629881a" /></ins></div>

✅ __Sheet: City_Targets__  
Columns include: City,	Monthly Target (USD)  
<div align="center"><img width="347" height="241" alt="image" src="https://github.com/user-attachments/assets/7522203f-eb15-40cf-85d7-f2388d459fc2" /></ins></div>

✅ __Sheet: Vendor_Contacts__  
Columns include: Vendor Name, Contact Name,	Email,	Phone
<div align="center"><img width="1157" height="577" alt="image" src="https://github.com/user-attachments/assets/b570e856-5978-4eca-a830-7da6bc4495e1" /></ins></div>

***

### <div align="center">Identification Issues</ins></div>
📌 __Tasks:__  
1️⃣ Combine and clean the data in the 'Sales_Data' sheet

2️⃣ Ensure all cities listed in the 'City_Targets' tab match those in your final output

3️⃣ Join city-level revenue totals with the 'City_Targets' table

4️⃣ Calculate the % of monthly target achieved for each city

5️⃣ Create a new summary that ranks cities based on performance

6️⃣ Extract a vendor contact list using the 'Vendor_Contacts' tab

7️⃣ Bonus: Add any charts or filters to enhance your analysis

***

### <div align="center">Solving Step or Analysis</ins></div>

***

### <div align="center">Results Overview</ins></div>
