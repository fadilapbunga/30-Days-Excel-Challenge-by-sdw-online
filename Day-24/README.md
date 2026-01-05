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
1️⃣ 

- First, clean the data in each sheet.
- The first thing you can do is ensure that there is __no duplicate data__ by going to __Home ➡️ Remove Rows ➡️ Remove Duplicates.__
- Ensure that there are __no extra spaces__ in any format containing text by __TRIM__ text.
- For the first sheet, which is the __Sales_Data sheet__, ensure that the format of each column is correct as shown below:

<div align="center">
  
Column         | Format
-------------  | -------------
Transaction ID | Text
Date           | Date
City           | Text
Product        | Text
Units Sold     | Number
Unit Price     | Decimal Number
Payment Method | Text
Total Revenue  | Decimal Number

</ins></div>

---
- For the next sheet, __City_Targets__, as with the previous sheet, ensure that the column format matches the format shown in the table below:

<div align="center">
  
Column                | Format
-------------         | -------------
City                  | Text
Monthly Target (USD)  | Number

</ins></div>

---
- Then the last sheet is __Vendor_Contacts__.
- Make sure there are no extra spaces in each column by using __TRIM__.
- Make sure the format of each column is correct according to the table below.

<div align="center">

Column         | Format
-------------  | -------------
Vendor Name    | Text
Contact Name   | Text
Email          | Text
Phone          | Number

</ins></div>

- After that, it was discovered that the data in the Phone column was incorrect or unclean. Therefore, further data cleaning was required so that the data could be used for future purposes.
- To do this, clean the Phone column, which was found to contain the following errors:  
⚠️ __Many different formats: (), +, -, .  
⚠️ There are country codes (+1, 001)  
⚠️ There are extensions (x506, x93133)__

Therefore, from this data cleaning, the expected data is as shown in the table below, consisting only of numbers and 10 digits.

<div align="center">

Before                  | After
-------------           | -------------
001-324-610-2489x506    | 3246102489
001-927-878-6537        | 9278786537
001-989-823-5151x93133  | 9898235151
(450)836-8713x8799      | 4508368713

</ins></div>

📝 The first thing to do in this data cleaning process is to delete the numbers after the letter ‘x’. If you notice, the letter after ‘x’ is always at the end of the digits, so this will be removed by going to __Transform ➡️ Extract ➡️ Text before Delimiter ➡️ Enter the delimiter ‘x’__. This will remove the digits after ‘x’ and leave only the previous digits.
<div align="center"><img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/458d4420-30b6-4692-8dde-63043823c3ee" /></ins></div>

---
📝 The next step is to only take characters 0-9 and delete all automatic symbols. Therefore, what you can do is create a new column named __phone_digits__ with the formula:
<div align="center"><img width="1920" height="1014" alt="image" src="https://github.com/user-attachments/assets/98b1c3c2-d5c2-4b3e-8dd4-794fc9fd0d58" /></ins></div>

---
📝 



***

### <div align="center">Results Overview</ins></div>
