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
Phone          | Text and Number

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
📝 After that, since we only need 10 digits of the number and there are some numbers that still have country codes (+1, 001), the country code will be removed using the formula below:
````excel
let
    p = [phone_digits]
in
    if Text.Length(p) = 11 and Text.Start(p,1) = "1" then Text.End(p,10)
    else if Text.Length(p) = 13 and Text.Start(p,3) = "001" then Text.End(p,10)
    else p
 ````
This means that, if explained carefully, the phone_digits column is assumed to be p to simplify the subsequent writing so that it is not too long. then if the length of the digits in the column is __11__ and it starts with the letter __1__, only take the last 10 digits, and likewise if the length of the digits in the column is __13__ and it starts with the letters __001__, only take the last 10 digits, and leave the rest as it is.

---
2️⃣    
To complete task No. 2, ensure that the data in the __Sales_Data__ and __City_Targets__ sheets is clean, meaning that there are no extra spaces and that the capitalization is correct. Once you have confirmed this, the next step to ensure that all cities listed in the ‘City_Targets’ tab match those in your final output is to:  
➡️ __Open query Sales_data  
➡️ Tab Home  
➡️ Click Merge Queries__
- First table: Sales_Data
- Second table: City_Targets
- Click the City column in BOTH tables
- Join kind: Left Anti (rows only in first)
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/0f1118d5-2fae-433d-92d5-5e18270b550f" /></ins></div>

- The result is __“This table is empty"__, it means an empty anti-join result indicates that all sales cities match the predefined target list.

---
3️⃣  
To join city-level revenue totals with the 'City_Targets' table, the following methods can be used:

➡️ First, create a duplicate query on the Sales_Data_Clean sheet.
➡️ Then, perform a __Group By__ operation to calculate the total revenue per city with the column name __‘City Revenue’__ using the __‘Sum’__ operation on __‘Total Revenue’__.
<div align="center"><img width="1920" height="1022" alt="image" src="https://github.com/user-attachments/assets/63233e6d-d187-4426-8287-ac72f1498943" /></ins></div>

➡️ Then merge the newly created column, “City Revenue,” into the City Targets sheet as shown below:
<div align="center"><img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/54db175b-c208-4a8e-8a3d-ef6123e47a39" /></ins></div>

➡️ Then the city-level revenue total has been merged with the City Targets sheet.
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/aba93b40-ebc8-47b7-88ec-2913f381d6a5" /></ins></div>

---
4️⃣  
➡️ To calculate the % of monthly target achieved for each city, create a new column named ‘Target Achieved (%)’ with the formula below:
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/22dd7751-067c-4112-a2bd-769642ed1eb2" /></ins></div>

➡️ Then convert it to percentage format by going to __Transform → Data Type → Percentage__
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/23d9efc4-937c-455e-8c04-5347ae63b344" /></ins></div>

---
5️⃣  
- To see which cities have the most achievement targets, you can first sort them by total achievements, as shown in the image below.
<div align="center"><img width="1920" height="1016" alt="image" src="https://github.com/user-attachments/assets/a146dfb3-58da-4d14-a9ea-1d68dccf6cf7" /></ins></div>

- Then, to find out the sequence/ranking based on the order above, use the __index column__ starting from 1 as shown in the image below.
<div align="center"><img width="1920" height="1016" alt="image" src="https://github.com/user-attachments/assets/fa2c4085-2d73-49c6-908a-bd43cbbe7a1d" /></ins></div>

---
6️⃣  
The vendor list extraction on the Vendor Contacts sheet has been done as per task no. 1. The extraction that has been done includes:
- Ensuring that there are no extra spaces in each column
- Ensuring that the data format is correct
- Cleaning the data in the ‘Phone’ column as per task no. 1
- Furthermore, ensuring that emails are written in lowercase letters
<div align="center"><img width="1027" height="579" alt="image" src="https://github.com/user-attachments/assets/cf37a221-bb8a-4a62-a353-c08e82835706" /></ins></div>

---
7️⃣









***

### <div align="center">Results Overview</ins></div>
