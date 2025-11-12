# 1️⃣3️⃣ Day 13: Data validation

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

### <div align="center">Identification Database</ins></div>
There is a dataset from HR to maintain clean employee records, and the dataset consists of the columns __Employee Name, Department, Age, Salary ($), Start Date, and Email.__
<img width="960" height="509" alt="image" src="https://github.com/user-attachments/assets/8b1d87f5-3125-42c1-8ed2-83a21a6dcafa" />

***

### <div align="center">Identification Issues</ins></div>
🎯 __Scenario__:

You're working in HR to maintain clean employee records.
Your job is to apply data validation rules to prevent bad data entry.

🔧 __Tasks__:

1️⃣ Age must be between 18 and 65.

2️⃣ Salary must be a number between 30,000 and 200,000.

3️⃣ Start Date must be between Jan 1, 2020 and today.

4️⃣ Emails must contain '@' and '.' characters.

5️⃣ Department must use a dropdown list: HR, IT, Sales, Finance, Marketing.

6️⃣ Add an input message to Age column: 'Enter age between 18 and 65'.

7️⃣ Add an error alert to Salary column: 'Salary must be between 30,000 and 200,000'.


***

### <div align="center">Solving Step or Analysis</ins></div>

1️⃣
- Choose column C:C is the __Age__ column to be validated using __Data Validation__
- Open the __Data menu → Data Validation__
- Select __“Allow: Whole Number”__
- Select __Data between 18 and 65__
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/93d1f713-de92-46f5-84a4-b95cd37ec0d0" />

---

2️⃣
- Choose column D:D is the __Salary($)__ column to be validated using __Data Validation__
- Open the __Data menu → Data Validation__
- Select __“Allow: Date”__
- Select __Data between Start Date: 2020-01-01 and End Date: =TODAY()__
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/2d3d2157-5221-4772-aabd-b90d3445ed97" />

---

3️⃣
- Choose column E:E is the __Start Date__ column to be validated using __Data Validation__
- Open the __Data menu → Data Validation__
- Select __“Allow: Whole Number”__
- Select __Data between 30.000 and 200.000__
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/53bf83d7-cd4f-4032-bd4b-2c9d6fc375df" />



***

### <div align="center">Results Overview</ins></div>
