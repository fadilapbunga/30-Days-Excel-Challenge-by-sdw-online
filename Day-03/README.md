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
    - Add new column D to create a 'Total Pay' and contains value which =B2 * C2, etc


***


## Results Overview
