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

1. Load the 'Asset_Log' table into Power Query.
2. Format the 'Asset Type' and 'Status' columns with Capitalize Each Word.
3. Remove duplicate asset records.
4. Fill in missing Department values using Fill Down (after sorting by Asset ID).
5. Add a flag column called 'Department Status' to label filled rows.
6. Unpivot 'Jan Usage', 'Feb Usage', and 'Mar Usage' into Month and Usage.
7. Clean 'Cost':
   - Replace 'N/A' and blank values with nulls
   - Convert column to decimal
   - Add a 'Cost Status' column to flag missing cost info

🎯 __Bonus:__

- Filter out any rows where usage is completely missing (nulls).

Once complete, click Close & Load to return the clean data to Excel.

***

### <div align="center">Solving Step or Analysis</ins></div>

***

### <div align="center">Results Overview</ins></div>
