# 2️⃣0️⃣ Day 20: Power Query

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

### <div align="center">Identification Database</ins></div>
🖥️ __Scenario: IT Asset Usage Cleanup__

You've been given a messy IT asset report that needs to be cleaned before sending it to leadership.

✅ __Sheet: 'Asset_Log'__

Columns include: Asset ID, Assigned User, Department, Asset Type, Monthly Usage (Jan–Mar), Status, Cost

<div align="center"><img width="1219" height="621" alt="image" src="https://github.com/user-attachments/assets/9c12a6a2-c0cf-4590-b53a-9fefcfe65b80" /></ins></div>

***

### <div align="center">Identification Issues</ins></div>
📌 __Tasks to Perform in Power Query:__

1️⃣ Load the 'Asset_Log' table into Power Query.

2️⃣Format the 'Asset Type' and 'Status' columns with Capitalize Each Word.

3️⃣ Remove duplicate asset records.

4️⃣ Fill in missing Department values using Fill Down (after sorting by Asset ID).

5️⃣ Add a flag column called 'Department Status' to label filled rows.

6️⃣ Unpivot 'Jan Usage', 'Feb Usage', and 'Mar Usage' into Month and Usage.

7️⃣ Clean 'Cost':
   - Replace 'N/A' and blank values with nulls
   - Convert column to decimal
   - Add a 'Cost Status' column to flag missing cost info

🎯 __Bonus:__

- Filter out any rows where usage is completely missing (nulls).

Once complete, click Close & Load to return the clean data to Excel.

***

### <div align="center">Solving Step or Analysis</ins></div>
1️⃣
- To load the ‘Asset_Log’ table into Power Query, the steps are as follows: __click on the table to be selected ▶️ then click Data ▶️ Get Data ▶️ From Other Sources -▶️ From Table/Range.__
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/d69229da-fc21-49b2-8b34-d54461ec5016" /></ins></div>

---
2️⃣
- To format the __'Asset Type'__ and __'Status'__ columns with Capitalize Each Word, the steps are as follow: __click Asset Type and Status Column ▶️ then click Transform ▶️ choose Format ▶️ click Capitalize Each Word__
<div align="center"><img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/a5c9b7ef-cf69-49c5-a6f5-89245e802bd1" /></ins></div>

---
3️⃣
- To remove duplicate asset records, the steps are as follow: __Click all columns ▶️ on Home, click Remove Rows ▶️ then click Remove Duplicates__
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/15705c21-ae7b-42f6-9460-05778e3473d7" /></ins></div>

---
4️⃣




***

### <div align="center">Results Overview</ins></div>
