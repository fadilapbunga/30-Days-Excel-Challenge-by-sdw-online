

# 7️⃣ Day 7: Practice (Week 1 review)

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

## Identification Database
To practice Week 1, there is a sheet with some variety column that contain data like: Department, Category, Month, Planned Budget (USD), Actual Spend (USD), and Notes. Like the picture below. And this sheet contains 500 rows.
<img width="960" height="509" alt="image" src="https://github.com/user-attachments/assets/f97af8ef-2acb-4271-b6b5-86597e80f83d" />

***

## Identification Issues
Based on the instruction, we were asked to track which departments are spending wisely and which are going over budget.
<img width="960" height="509" alt="image" src="https://github.com/user-attachments/assets/6d0dd7ea-7340-4722-804f-197927a34591" />


***

## Solving Step or Analysis
1. Create new column and give it named 'Budget Status' and then fill in the following formula:
  ````excel
		=IF($E2<=$D2;"On Budget";"Over Budget")
 ````
if the actual spend is more than planned budget, it's over budget and vice versa.
<img width="960" height="508" alt="image" src="https://github.com/user-attachments/assets/6b91c853-dbe0-4b2c-bdfe-8a40e9924926" />

***

2. Create pivot table with range the table and fill in the field pivot table with 'Department' into Rows and 'Planned Budget' & 'Actual Spend' into Values.
<img width="960" height="509" alt="image" src="https://github.com/user-attachments/assets/68c271bf-79b0-42f6-8c33-e4bbbf09b17e" />

***

3. To see a rough visualization of the planned budget and actual spend, the image below uses a bar chart to visualize this information. The bar chart named 'Actual Spend Vs Planned Budget'. I add data label which the white number is the planned budget and the red number is the actual spend.
<img width="960" height="508" alt="image" src="https://github.com/user-attachments/assets/df0d7118-6a56-4558-bec9-07d1887dbef5" />

***

4. Here i try to highlight rows where overspend exceeds 20% of planned budget in 'Budget Status' column. Where i use Edit Formatting Rule. First calculate how much the expenditure exceeds the initial budget.
````excel
		=(Actual Spend - Planned Budget)/Planned Budget
 ````
  and then if the expenditure exceeds the initial budget more than 20% or 0.2, mark the text with red fill.
<img width="960" height="493" alt="image" src="https://github.com/user-attachments/assets/aac6546a-f1ca-43d1-afb4-a72e08e44c98" />

***

5. And for optional, add the data bar in 'Actual Spend' column. Those with the highest expenditure have the longest bar data
<img width="1920" height="1017" alt="image" src="https://github.com/user-attachments/assets/88a76e60-783a-45d5-b5b4-e64d891f6167" />



***


## Results Overview
1. There are 277 that are over budget, and 223 that are on budget.
2. - Sum of Planned Budget ($) =  2.756.656
   - Sum of Actual Spend =  3.181.620
   - The difference between the two is 424,964. And expenses exceed income, so it is clearly a loss.
3. The image graph shows that the HR and IT departments have many expenses.
4. 232 that are over budget by more than 20% of the planned budget.
