# 1️⃣2️⃣ Day 12: Pivot tables – part 2

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

### <div align="center">Identification Database</ins></div>
There is a dataset consisting of the columns __Ticket ID, Date Submitted, Issue Type, Priority, Platform, Category, Status, Time to Resolution (hrs), and User Rating (1-5)__. As shown in the image below:
<img width="960" height="511" alt="image" src="https://github.com/user-attachments/assets/65a80ba4-64ac-4f55-9af7-e2b5342a8dc0" />

***

### <div align="center">Identification Issues</ins></div>
You're part of a Customer Support team at a tech company. The leadership team needs insights from the support ticket system to improve operations.

✅ __Tasks:__
1. Which issue types are reported most often?
   - Use a pivot table with Issue Type in Rows, Count of Ticket ID in Values.

2. Which platform generates the most support tickets?
   - Use Platform in Rows, Count of Ticket ID in Values.

3. What's the average resolution time by priority?
   - Priority in Rows, Average of Time to Resolution in Values.

4. Which ticket category has the lowest user rating?
   - Category in Rows, Average of User Rating in Values. Apply conditional formatting.

5. How do ticket counts trend month-by-month?
   - Group Date Submitted by Month in Rows, Count of Ticket ID in Values.

📌 __Bonus:__
- Add a Timeline to filter by date
- Try a calculated field for something like Satisfaction per Hour: User Rating / Time to Resolution

***

### <div align="center">Solving Step or Analysis</ins></div>
 
- First, check the data to see if it is neat and in the correct format __(Data Cleaning)__.
- The data below shows that the format in the __Date Submitted__ column is still messy, so the data format is changed to __dd-mm-yyyy__ so that the data only displays the desired date.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/dd0c1fef-5096-4efc-aa8e-38391e44bbaf" />
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/48f91fe2-aaf0-479f-be0e-8a5cebf5f8f9" />

---

1️⃣
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/457e3c7f-baf2-45d5-b808-44c3083ee6f0" />

---

2️⃣
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/64ea0e47-39a0-4dc9-8962-6efb35601522" />

---

3️⃣
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/a2109937-e89e-4844-97e1-91626c7cf4d0" />


---

4️⃣
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/8eef1cbe-17e6-4b80-8bbc-56e633443f9d" />


---

5️⃣
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/f238a474-7e36-43ee-bb9e-cf0dc99ced60" />

---

📌 __Bonus__

<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/66332570-5b51-41d2-9e2d-c36888edd4f0" />
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/b4a4e930-aab3-4d89-b9bb-a6b0c0dc5484" />



---
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/4311eeea-8431-4b4f-a292-5e1223c5b280" />


***

### <div align="center">Results Overview</ins></div>
<img width="825" height="263" alt="image" src="https://github.com/user-attachments/assets/e5d9cfb5-bf5d-4d01-aac7-52e406812a65" />

