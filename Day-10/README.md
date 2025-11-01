# 🔟 Day 10: Aggregate functions

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

### <div align="center">Identification Database</div>
This time, the data training is operations data from multiple fitness club branches. For example:
<img width="960" height="508" alt="image" src="https://github.com/user-attachments/assets/ec3256df-d6f2-4e03-b8fd-947ea71ca7c8" />

***

### <h2 align="center">Identification Issues</h2>
You're working with operations data from multiple fitness club branches.
Your job is to summarize spending and activity using Excel’s aggregate functions.

✅ __Task 1: Total Expense by Branch__
Use =SUMIF(A:A, "Downtown", D:D) to get total cost for each branch.

✅ __Task 2: Count of Purchases per Department__
Use =COUNTIF(B:B, "Marketing") to count how many transactions came from a specific department.

✅ __Task 3: Find Most & Least Expensive Purchases__
Use =MIN(D:D) and =MAX(D:D) on Expense ($) column.

✅ __Task 4: Calculate Average Spend__
Use =AVERAGE(D:D) to find average expense across the board.

✅ __Task 5: Conditional Formatting__
Highlight Expense > $10,000 using Conditional Formatting → Highlight Cell Rules → Greater Than

📌 __BONUS:__
Try COUNTIFS to count purchases in Marketing that spent over $5000
Example: =COUNTIFS(B:B,"Marketing",D:D,">5000")

These functions help you find spending patterns across clubs quickly.

***

### Solving Step or Analysis

✅ __Task 1: Total Expense by Branch__

- Calculate total expenses per branch using __=SUMIF__ with criteria from each branch. The sum range is in column D (Expenses).

<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/b3c077e7-a67c-4472-a02f-37eece6bc776" />

***

✅ __Task 2: Count of Purchases per Department__

- Count of Purchases per Department can be used to find out which department has the most transactions, therefore the __=COUNTIF__ formula is used to calculate how many transactions are made per department.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/1a54bc8d-2efb-4d83-bcfd-5053af5aae05" />


***

✅ __Task 3: Find Most & Least Expensive Purchases__

- For the most expensive, use the formula __=MAX__ to find the largest value in the expenses, and the Expense ($) column is in column D.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/cfdd34ae-77dc-4dd2-901b-6ea855935853" />

- For the least expensive, use the formula __=MIN__ to find the least value in the expenses, and the Expense ($) column is in column D.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/41ce76b5-11f6-4248-bd72-e0e3e7816026" />

***

✅ __Task 4: Calculate Average Spend__

- The formula __=AVERAGE(E2:E100)__ is applied to the Expenses column to obtain the average expenditure value from all data rows. This formula adds up all values in the Expenses column and then divides them by the number of data points calculated.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/b6fcb55f-d9a3-40ee-b8df-3265ad73ba92" />

***

✅ __Task 5: Conditional Formatting__

- Use __Conditional Formatting__ with rules for expenses over 10,000 and give them a green fill color.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/e8f95281-79af-4649-9b05-c8e996f7cc4c" />

***

📌 __BONUS__

- Using the __=COUNTIFS__ formula when you need to count data based on more than two conditions. Here, the first condition is to count data from the marketing department, and the second condition is that the expense is more than 5000.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/c57a56b3-09c1-48f4-9090-00ee28ab5f03" />


### Results Overview
- Total expenses were successfully calculated per branch using the __SUMIF__ function, resulting in the highest value in the Downtown branch at $713,131 and the lowest in Uptown at $563,124.
- Using __COUNTIF__, we can find out which departments have the most transactions, namely the Staff department with 85, and the lowest are in Marketing and Maintenance.
- Find the most expensive item, which is 15,970, using the __MAX__ formula, and the least expensive item, which is 1,624, using the __MIN__ formula.
- On average, each department and branch spends 8354 of the total and calculates this average spend using the __AVERAGE__ formula.
- __Conditional Formatting__ is applied to the Expenses column with the rule that values above 10,000 are colored green. As a result, data with large expenses can be identified immediately without the need for manual calculation.
- There are 46 people from the marketing department who spent more than 5000, calculated using the __COUNTIFS__ formula.
