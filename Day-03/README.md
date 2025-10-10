# 3️⃣ Day 3: Formulas and functions

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

## Identification Database
The file have 4 Sheets, each sheet contains data with approximately 100+ different records, but they are all part of a single entity. Therefore, this is approximately the data content of each sheet.

**1. Freelance Tracker**                                        
   
| Freelancer | Hours Worked | Hourly Rate ($) |
| ---------  | ------------ |---------------- |
| John       | 45           |34               |
| Dana       | 50           |71               |
| Katie      | 39           |35               |
| ......     | ......       |......           |

**2. Ad Spend**

| Platform | Ad Budget ($) | 
| ---------| ------------- |
| Twitter  | 962           |
| Twitter  | 838           |
| Facebook | 1324          |
| ......   | ......        |     

**3. Online Orders**

| Order ID | Item Price | Tax % |
| ---------| ---------- |------ |
| 1000     | 167        |0,07   |
| 1001     | 59         |0,1    |
| 1002     | 125        |0,08   |
| ......   | ......     |...... |

**4. Tuition Calculator**

| Student | Base Tuition ($) | Scholarship (%) |
| --------| ---------------- |---------------- |
| Melissa | 11191            |0,20             |
| Caroline| 12029            |.....            |
| David   | 12312            |.....            |
| ......  | ......           |......           |


***

## Identification Issues
Sheets & Tasks:

**1. Freelance Tracker:**
   - Create a 'Total Pay' column using: =B2 * C2
   - Use functions to calculate: SUM (hours), AVERAGE (rates), MIN and MAX

**2. Ad Spend:**
   - Add a 'Platform Fee' column at 10% of Ad Budget: =B2 * 0.10
   - Drag the formula down (Relative Reference)

**3. Online Orders:**
   - Add a 'Tax Amount' column using: =B2 * C2 (row-level tax)
   - Drag formula down to apply to all 100+ orders

**4. Tuition Calculator:**
   - Use absolute reference to apply 20% scholarship to all rows
   - Only row 1 contains the rate, so use: =B2 * $C$2


***

## Solving Step or Analysis

**1. Freelance Tracker:**
  
- Add new column D to create a 'Total Pay' and contains value which =B2 * C2, etc. Change the 'Hourly Rate' into Dollar US format so when the Hours Worked values multiply with Hourly Rate ($) values the result is in Dollar. 
<img width="960" height="509" alt="Image" src="https://github.com/user-attachments/assets/71205efc-984d-4a62-9a77-51de20a6aeb5" />

***

- To get total of Hours Worked, use the formula =SUM(B2:B101), this formula sums the total hours worked from 100+ rows. And the result obtained is 3496 hours.
- To get the average of Hourly, Rate use the formula =AVERAGE(C2:C101), this formula sums the average hourly rated from 100+ rows. And the result obtained is $58.
- For the maximum value of total pay, use the formula =MAX(D2:D101), which gives a value of $3760. For the minimum value of total pay, use the formula =MIN(D2:D101), which gives a value of $770.
<img width="960" height="510" alt="Image" src="https://github.com/user-attachments/assets/69e0c4cc-4876-42fb-b11d-c8caa8ce651c" />

***

**2. Ad Spend**

- Add new column C to create a 'Platform Fee' and contain value which =$B2*0,1. The platform fee charged for each ad budget is 10%. And drag all the formula down.
<img width="1920" height="1018" alt="Image" src="https://github.com/user-attachments/assets/268538e6-b3f7-4fb7-bfd4-8c2480f584b8" />

***

**3. Online Orders:**

- Add new column D to create a 'Tax Amount' and contain value which =$B2*$C2. And drag all the formula down.
<img width="1920" height="1015" alt="Image" src="https://github.com/user-attachments/assets/58b17402-29cd-4a4d-a201-56683dc61360" />

***

**4. Tuition Calculator:**

- Add new column D to create a 'Scholarship Amount' and contain value which =$B2*$C$2, where $C$2 is the referred cell remains constant and doesn’t change when it is copied.
<img width="1918" height="1021" alt="Image" src="https://github.com/user-attachments/assets/9552c5ae-9bc1-4948-849e-fe37d62f8fc8" />

***

## Results Overview
In Freelance Tracker sheet, total income is calculated by multiplying the number of hours worked by the hourly rate, then applying aggregate functions such as SUM, AVERAGE, MIN, and MAX to analyze the data as a whole.

In the Ad Spend sheet, a Platform Fee column is added, amounting to 10% of the advertising budget, using relative references so that the formula can be easily applied to all rows. Meanwhile, in Online Orders sheet, the Tax Amount column is calculated based on the tax per row and is also copied to all order data using the same reference technique.

For the Tuition Calculator sheet, an absolute reference is used so that one scholarship value (20%) can be automatically applied to all rows without changing when the formula is copied down.

Overall, this task demonstrates the ability to use cell references (relative and absolute), basic Excel functions (SUM, AVERAGE, MIN, MAX), and create automatic formulas to calculate various data needs efficiently and accurately.
