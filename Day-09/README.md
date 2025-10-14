# 9️⃣ Day 9: Text functions

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

## Identification Database
To practice this function, it consists of data with messy writing formats as shown in the image below.
<img width="960" height="509" alt="image" src="https://github.com/user-attachments/assets/c665840f-8e2d-4da4-8935-9f53bff12ad1" />

***

## Identification Issues
Today’s challenge is to clean and transform messy text data using Excel’s text functions.
You’ll work with customer orders and apply formulas to make the data clean, structured, and ready for analysis.

✅ Task 1: Clean the Order ID
Use =UPPER(A2) to make all Order IDs uppercase.

✅ Task 2: Standardize Customer Names
Use =PROPER(B2) to format names like "jOHN sMITH" into "John Smith"

✅ Task 3: Trim Product Names
Use =TRIM(C2) to remove unwanted spaces.

✅ Task 4: Extract Product Code Details
Use =MID(E2,5,LEN(E2)-4) to extract the unique product ID after "PRD-".

✅ Task 5: Split Full Name into First and Last Name
First Name: =LEFT(B2, FIND(" ", B2)-1)
Last Name: =IF(ISNUMBER(FIND(" ", B2)), RIGHT(B2, LEN(B2)-FIND(" ", B2)), "No Last Name")

✅ Task 6: Count Product Name Length
Use =LEN(C2) to count number of characters in each product name.

🎨 BONUS – Add Conditional Formatting
- Yellow Fill: Quantity >= 3
- Red Fill: Customers with "No Last Name"

✅ Now turn your cleaned columns into a structured table.
Sort or filter to analyze the data efficiently.

***

## Solving Step or Analysis

<img width="1920" height="1017" alt="image" src="https://github.com/user-attachments/assets/f1a4bfc8-d9cb-4fb6-9683-2a7b53d40140" />

***

<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/f0eb1fca-b130-47d3-a3b7-f578aaa7ff85" />

***

<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/f4e49a4d-41ab-4432-90ce-190032ec65e6" />
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/287210da-8870-418d-aa05-860a2f7d5778" />

***



## Results Overview

***
