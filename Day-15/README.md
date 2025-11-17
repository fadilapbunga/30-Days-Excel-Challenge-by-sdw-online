# 1️⃣5️⃣ Day 15: Conditional formatting – part 2

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

### <div align="center">Identification Database</ins></div>
There is a dataset from the e-commerce operations team. The dataset consists of the column __Order Number, Client, Item	Date of Purchase, Amount Paid ($), Current Status, and Margin (%).__
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/9ec799ba-9bff-49ba-a914-183d8b28476a" />


***

### <div align="center">Identification Issues</ins></div>
You’ve received a dataset from the e-commerce operations team.
Your task is to highlight key insights using conditional formatting.

🔎 __Instructions:__

1️⃣ Highlight all orders placed on a weekend (Saturday or Sunday).

2️⃣ Highlight customers who spent more than $12,000.

3️⃣ Apply icon sets to the 'Margin (%)' column:
   - Green for margins above 40%
   - Yellow for margins between 15% and 40%
   - Red for margins below 15%
    
4️⃣ Highlight rows where:
   - The order is not marked as 'Completed'
   - And the purchase date is more than 30 days ago
     
5️⃣ Highlight orders with profit margins greater than 50%.


📌 __Bonus (Optional):__
- Create a Pivot Table to show total spend by Item.
- Highlight the top 10% of products based on total spend using conditional formatting.

***

### <div align="center">Solving Step or Analysis</ins></div>

- First, convert the data into a table format by pressing __CTRL + T__.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/020d1ed8-0d70-4675-822f-fc7bed05143d" />

---

- Then, clean the data by checking whether the data format is correct. If the __Date of Purchase__ format is still incorrect, change the format to __‘dd-mm-yyyy’__.
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/934b93c3-aa42-4134-aa03-ca2f60e486ea" />

---

1️⃣
- To highlight all orders placed on a weekend (Saturday or Sunday), use the formula __=WEEKDAY__ because the result will be returned to the number on that day in the selected cell date. For example, if the date is __11/17/2025 (today)__, then using the formula __=WEEKDAY__ will return the number __1__ because today is __Monday__, and __Monday is the first day of the week__. Weekends (Saturday or Sunday) are the __6th and 7th days of the week__, so the formula used is as follows:
````excel
		=WEEKDAY($D2;2)>=6
 ````

<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/d190ba77-2a4c-4058-9ca6-079c8e2cb918" />

---


2️⃣
- Highlight customers who spent more than $12,000 using Conditional Formatting Custom with formula: __=$E2>12000__
<img width="1920" height="1016" alt="image" src="https://github.com/user-attachments/assets/82072278-4cef-4274-ad1f-8aaa4312b114" />

---


3️⃣
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/400bd759-1ed3-41e5-af00-10aff646b34b" />

---

4️⃣
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/5c749f55-0eef-4a1a-83d6-5a880f40a5f9" />

---


5️⃣
<img width="1920" height="1014" alt="image" src="https://github.com/user-attachments/assets/42370c8d-81a1-48f9-914e-3e646c05280d" />

---

<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/4656c24a-2a32-47b9-aa4b-15d267da4f2d" />
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/7ed25583-7edb-413d-9946-6bacf586be54" />
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/71210aa3-8880-4497-aa6d-76ef0c521c20" />







***

### <div align="center">Results Overview</ins></div>
