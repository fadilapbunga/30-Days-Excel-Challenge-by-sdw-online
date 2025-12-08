# 1️⃣9️⃣ Day 19: Data cleaning

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

### <div align="center">Identification Database</ins></div>

🛒 __Scenario: Messy Product Catalog (E-commerce)__

You've received a messy export of your product catalog from multiple sellers.
Your task is to clean and standardize the dataset before it's used for dashboard reporting.

✅ __Sheet: ProductCatalog__

Columns include: Product ID, Product Name, Category, Price, Brand

<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/2dc2d6bf-3a40-46e5-aa85-66ea063a1833" />

***

### <div align="center">Identification Issues</ins></div>
📌 __Tasks:__

1️⃣ Identify and highlight duplicate records (hint: use a helper column to combine fields).

2️⃣Fix inconsistent casing in Product Names and Brand columns using PROPER().
3. Standardize the Category column (hint: use Find & Replace).
4. Clean up extra spaces using TRIM().
5. Convert inconsistent Price values into standard numeric format.
6. Replace any missing or empty values with 'Not Available' using Find & Replace.
7. Remove duplicate rows using Remove Duplicates.

🎯 __Bonus:__ Use LEN() to count characters before and after TRIM to demonstrate impact of cleaning.

🎯 __Bonus:__ Filter or conditional format blanks in key columns to spot issues fast.

***

### <div align="center">Solving Step or Analysis</ins></div>
1️⃣
- First, convert the data into table format.
- To make it easier to identify and highlight duplicate records, use an additional column as shown in the image below, which combines all the text from each column into one sentence using the formula:

````excel
        =[@[Product ID]]&[@[Product Name]]&[@Category]&[@Price]&[@Brand]
 ````
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/5d7e3568-4dcd-42de-ba36-230be9958d5d" /></ins></div>

---

- Then click __Remove Duplicates__ on the __Data Ribbon__ and make sure all columns are checked to find out which data is duplicated.
<div align="center"><img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/a4f41835-5dd9-4082-bf41-53d4008d0581" /></ins></div>

---

- It turns out that after checking, there is no duplicate data in this table.
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/cac69ebf-50af-4b96-83d8-268403674a04" /></ins></div>

---

- To ensure that there is no duplicate data in this table, you can highlight duplicates in __the helper column, Unique Record Identify__, by following these steps:
1. Block the Unique Record Identify column.
2. Conditional Formatting -> Highlight Cells Rules -> Duplicate Values.
3. Ensure that the selected cell format is data containing duplicates.
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/5aaa70a1-12db-468f-bd80-fc05ccc33a36" /></ins></div>
After doing so, it turned out that the results were the same, namely that no duplicate data was found. And there was no data highlighted in red. Therefore, the data from this table has been confirmed to be safe from duplicate data.

---
2️⃣





***

### <div align="center">Results Overview</ins></div>
