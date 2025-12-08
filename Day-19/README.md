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

3️⃣Standardize the Category column (hint: use Find & Replace).

4️⃣Clean up extra spaces using TRIM().
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

- To fix inconsistent casing in Product Names and Brand columns, use the helper columns titled __proper_ProductName__ and __proper_Brand__ with the formula __=PROPER.__
<div align="center"><img width="1928" height="1202" alt="image" src="https://github.com/user-attachments/assets/47ab86da-d1a6-4689-bd0a-2af011e7396c" /></ins></div>

---
- Then __Copy and Paste the Values__ into the original table to transfer the results
<div align="center"><img width="1920" height="1016" alt="image" src="https://github.com/user-attachments/assets/497fe1e1-5e0b-4cab-9887-3dd155255301" /></ins></div>

---
3️⃣

- To standardize the Category column, we reuse the __helper column__ as in __column L__, then duplicate the data in the Category column, and perform __Remove Duplicates__ as shown in the image below to extract the unique name of each category.
<div align="center"><img width="1920" height="1016" alt="image" src="https://github.com/user-attachments/assets/61527ea1-d283-490f-8ca1-ec3acb603479" /></ins></div>

- It is known that there are __7__ unique values remaining, including empty values.
<div align="center"><img width="1920" height="1014" alt="image" src="https://github.com/user-attachments/assets/d10f4e34-a05a-48b8-abc0-d4a152fe52b5" /></ins></div>

- After extracting the unique names in each category, create an additional helper column next to it with __a green fill color__ and the correct category name.
<div align="center"><img width="1920" height="1016" alt="image" src="https://github.com/user-attachments/assets/46cd8aa6-f875-4b96-9bbd-7683c20c173a" /></ins></div>

---

<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/25dcd163-69fc-4db7-94a5-8e2984c67933" /></ins></div>
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/abb10540-ac59-43c2-a4ff-e090e853e944" /></ins></div>
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/2e66ee04-a8d8-4ccf-be9d-d7b6b93378cc" /></ins></div>
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/02227a62-c5ed-4f9f-beff-b270dbeb158e" /></ins></div>

---
4️⃣











***

### <div align="center">Results Overview</ins></div>
