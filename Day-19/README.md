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

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6773529a-f117-4e83-b5aa-89dd25594000" />

***

### <div align="center">Identification Issues</ins></div>
📌 __Tasks:__
1. Identify and highlight duplicate records (hint: use a helper column to combine fields).
2. Fix inconsistent casing in Product Names and Brand columns using PROPER().
3. Standardize the Category column (hint: use Find & Replace).
4. Clean up extra spaces using TRIM().
5. Convert inconsistent Price values into standard numeric format.
6. Replace any missing or empty values with 'Not Available' using Find & Replace.
7. Remove duplicate rows using Remove Duplicates.

🎯 __Bonus:__ Use LEN() to count characters before and after TRIM to demonstrate impact of cleaning.

🎯 __Bonus:__ Filter or conditional format blanks in key columns to spot issues fast.

***

### <div align="center">Solving Step or Analysis</ins></div>

***

### <div align="center">Results Overview</ins></div>
