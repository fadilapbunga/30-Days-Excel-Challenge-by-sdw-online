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
- To format the __'Asset Type'__ and __'Status'__ columns with Capitalize Each Word, the steps are as follow: __Click Asset Type and Status Column ▶️ then click Transform ▶️ choose Format ▶️ click Capitalize Each Word__
<div align="center"><img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/a5c9b7ef-cf69-49c5-a6f5-89245e802bd1" /></ins></div>

---
3️⃣
- To remove duplicate asset records, the steps are as follow: __Click all columns ▶️ on Home, click Remove Rows ▶️ then click Remove Duplicates__
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/15705c21-ae7b-42f6-9460-05778e3473d7" /></ins></div>

---
4️⃣
- To fill in missing Department values using Fill Down (after sorting by Asset ID), the steps are as follow: __Click Department Column ▶️ Sort Ascending ▶️ and then click Transform ▶️ Fill Down__
<div align="center"><img width="1920" height="1016" alt="image" src="https://github.com/user-attachments/assets/0484d7df-9819-4245-aad3-8eb7f2d2e223" /></ins></div>
<div align="center"><img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/d48d9a30-ae09-4629-b58d-d55aaa577e74" /></ins></div>

---
5️⃣
- Add a marker for the department that must be filled in by adding a __Custom Column__ named __Department_Custom__ with the formula below:
````excel
    = if [Department] = null or Text.Trim([Department]) = ""
      then "Filled" else "Original"
 ````

This means that if the data says __‘Filled’__, it can be a marker that the department column must be filled in.
<div align="center"><img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/8ed18101-8421-49ec-82c1-c3f8c119cae4" /></ins></div>

---
6️⃣
- To unpivot 'Jan Usage', 'Feb Usage', and 'Mar Usage' into Month and Usage, the steps are as follow: __Click the selected column ▶️ Transform ▶️ Unpivot Column__
<div align="center"><img width="1920" height="1016" alt="image" src="https://github.com/user-attachments/assets/309fb088-6c2f-499d-a88c-4bae115f665c" /></ins></div>

---

- Rename the columns to __“Months” and “Usage”__
<div align="center"><img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/d1ca24ab-c96c-4863-ad07-e69995da52e2" /></ins></div>
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/e0dc6ba1-735f-44ac-8405-6708491599ee" /></ins></div>

---

- To tidy up the text in the __“Months”__ column, only extract __the month without the word “usage".__ To do this, use __Extract Text__, where __Text Before Delimiter__ and the delimiter are __spaces__.
<div align="center"><img width="1920" height="1022" alt="image" src="https://github.com/user-attachments/assets/9dfb1eda-2110-4145-959d-caea21fa57df" /></ins></div>

---
7️⃣

- To tidy up the Cost column, there are several things that must be done, including:
- Change every __N/A__ word to null in __Transform ▶️ Replace Values.__ To change it to null, simply leave it blank and click OK.
<div align="center"><img width="1920" height="1022" alt="image" src="https://github.com/user-attachments/assets/c6083685-73fd-4835-bf17-0daf78273e16" /></ins></div>

---

- Before further tidying up, the column units to be used must be determined. It was agreed that the __Cost__ column would contain values in __US dollars__, so to make the data easier to read, a small note was added to the Cost column heading, changing it to __Cost ($).__
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/a6baa931-7f88-4d19-aa7e-5505bd23b5b7" /></ins></div>

---

- It appears that the Cost ($) column contains several improper word choices, as shown in the image below:
<div align="center"><img width="1920" height="868" alt="image" src="https://github.com/user-attachments/assets/16ae5409-6b79-442c-9c56-460b512d8120" /></ins></div>

---

- The next step is to convert each improper data into __1200__ (in dollars). Use __Transform ▶️ Replace Values.__
<div align="center"><img width="578" height="867" alt="image" src="https://github.com/user-attachments/assets/3918dec8-79fd-46c1-9fc8-3879f4cd685e" /></ins></div>

--- 

- The next step is to change the format of the __Cost($) column to Decimal Number__ by clicking the small arrow next to the Cost ($) heading and changing it to Decimal Number, as shown below.
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/77c4fa61-02a8-4985-953b-5e9a0beedba1" /></ins></div>


---

- To make it easier to indicate whether the Cost ($) value has been filled in or not, you can use an additional column in: __Add Column ▶️ Custom Column ▶️ named Cost Status, and the formula is as follows:__
````excel
    =if [#"Cost($)"] = null then "Missing" else ""
 ````
This means that if the column is equal to null, I only want to mark it with the word “Missing,” but if not, then it will be left blank without a mark.
<div align="center"><img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/ba360fc3-3b26-45e2-88c0-ad37f2f3da01" /></ins></div>

---

<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/09af817e-3ad9-4866-b59e-38d9bd614177" /></ins></div>
<div align="center"><img width="1383" height="581" alt="image" src="https://github.com/user-attachments/assets/a6949d3d-b41c-46d5-941d-eee6b33ebb0f" /></ins></div>
















***

### <div align="center">Results Overview</ins></div>
