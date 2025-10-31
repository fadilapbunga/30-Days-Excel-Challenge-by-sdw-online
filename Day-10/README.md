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

- Calculate total expenses per branch using SUMIF with criteria from each branch. The sum range is in column D (Expenses).

<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/b3c077e7-a67c-4472-a02f-37eece6bc776" />

***

✅ Task 2: Count of Purchases per Department

- Count of Purchases per Department can be used to find out which department has the most transactions, therefore the COUNTIF formula is used to calculate how many transactions are made per department.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/1a54bc8d-2efb-4d83-bcfd-5053af5aae05" />


***

✅ Task 3: Find Most & Least Expensive Purchases

- For the most expensive, use the formula =MAX to find the largest value in the expenses, and the Expense ($) column is in column D.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/cfdd34ae-77dc-4dd2-901b-6ea855935853" />

- For the least expensive, use the formula =MIN to find the least value in the expenses, and the Expense ($) column is in column D.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/41ce76b5-11f6-4248-bd72-e0e3e7816026" />

***

✅ Task 4: Calculate Average Spend

- The formula =AVERAGE(E2:E100) is applied to the Expenses column to obtain the average expenditure value from all data rows. This formula adds up all values in the Expenses column and then divides them by the number of data points calculated.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/b6fcb55f-d9a3-40ee-b8df-3265ad73ba92" />

***

✅ Task 5: Conditional Formatting

- Use conditional formatting with rules for expenses over 10,000 and give them a green fill color.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/e8f95281-79af-4649-9b05-c8e996f7cc4c" />

***

📌 BONUS

- Using the COUNTIFS formula when you need to count data based on more than two conditions. Here, the first condition is to count data from the marketing department, and the second condition is that the expense is more than 5000.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/c57a56b3-09c1-48f4-9090-00ee28ab5f03" />


## Results Overview
- Total expenses were successfully calculated per branch using the SUMIF function, resulting in the highest value in the Downtown branch at $713,131 and the lowest in Uptown at $563,124.
- Using COUNTIF, we can find out which departments have the most transactions, namely the Staff department with 85, and the lowest are in Marketing and Maintenance.
- Find the most expensive item, which is 15,970, using the MAX formula, and the least expensive item, which is 1,624, using the MIN formula.
- On average, each department and branch spends 8354 of the total and calculates this average spend using the AVERAGE formula.
- Conditional Formatting is applied to the Expenses column with the rule that values above 10,000 are colored green. As a result, data with large expenses can be identified immediately without the need for manual calculation.
- There are 46 people from the marketing department who spent more than 5000, calculated using the COUNTIFS formula.
