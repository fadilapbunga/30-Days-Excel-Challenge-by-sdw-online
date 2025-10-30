# 🔟 Day 10: Aggregate functions

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

## Identification Database
This time, the data training is operations data from multiple fitness club branches. For example:
<img width="960" height="508" alt="image" src="https://github.com/user-attachments/assets/ec3256df-d6f2-4e03-b8fd-947ea71ca7c8" />

***

## Identification Issues
You're working with operations data from multiple fitness club branches.
Your job is to summarize spending and activity using Excel’s aggregate functions.

✅ Task 1: Total Expense by Branch
Use =SUMIF(A:A, "Downtown", D:D) to get total cost for each branch.

✅ Task 2: Count of Purchases per Department
Use =COUNTIF(B:B, "Marketing") to count how many transactions came from a specific department.

✅ Task 3: Find Most & Least Expensive Purchases
Use =MIN(D:D) and =MAX(D:D) on Expense ($) column.

✅ Task 4: Calculate Average Spend
Use =AVERAGE(D:D) to find average expense across the board.

✅ Task 5: Conditional Formatting
Highlight Expense > $10,000 using Conditional Formatting → Highlight Cell Rules → Greater Than

📌 BONUS:
Try COUNTIFS to count purchases in Marketing that spent over $5000
Example: =COUNTIFS(B:B,"Marketing",D:D,">5000")

These functions help you find spending patterns across clubs quickly.

***

## Solving Step or Analysis

✅ Task 1: Total Expense by Branch
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/b3c077e7-a67c-4472-a02f-37eece6bc776" />

***

✅ Task 2: Count of Purchases per Department
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/1a54bc8d-2efb-4d83-bcfd-5053af5aae05" />


***

✅ Task 3: Find Most & Least Expensive Purchases
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/cfdd34ae-77dc-4dd2-901b-6ea855935853" />
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/41ce76b5-11f6-4248-bd72-e0e3e7816026" />

***

✅ Task 4: Calculate Average Spend
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/b6fcb55f-d9a3-40ee-b8df-3265ad73ba92" />

***

✅ Task 5: Conditional Formatting
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/e8f95281-79af-4649-9b05-c8e996f7cc4c" />

