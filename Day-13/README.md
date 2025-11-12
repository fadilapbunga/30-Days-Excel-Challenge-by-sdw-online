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
- Select __"Data between 18 and 65"__
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/93d1f713-de92-46f5-84a4-b95cd37ec0d0" />

---

2️⃣
- Choose column D:D is the __Salary($)__ column to be validated using __Data Validation__
- Open the __Data menu → Data Validation__
- Select __“Allow: Whole Number”__
- Select __"Data between 30.000 and 200.000"__
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/2d3d2157-5221-4772-aabd-b90d3445ed97" />

---

3️⃣
- Choose column E:E is the __Start Date__ column to be validated using __Data Validation__
- Open the __Data menu → Data Validation__
- Select __“Allow: Date”__
- Select __"Data between Start Date: 2020-01-01 and End Date: =TODAY()"__
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/53bf83d7-cd4f-4032-bd4b-2c9d6fc375df" />

---

4️⃣
- Choose column F:F is the __Email__ column to be validated using __Data Validation__
- Open the __Data menu → Data Validation__
- Select __“Allow: Custom”__
- Enter the following formula:

````excel
		=AND(ISNUMBER(SEARCH("@";F2)); ISNUMBER(SEARCH(".";F2)))
 ````

- The meaning of the above formula is that if the formula __=SEARCH__ finds the symbols __'@'__ and __'.'__, the result of the formula will be returned as __TRUE__ using the formula __=ISNUMBER__. __=AND__ formula is used because there are two characters that must meet the criteria.

<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/23471e60-21f4-4d45-b8ef-637444611bb5" />

---

5️⃣
- First, find the __unique name__ of each __Department column__
- Copy the data of department column in column H
- Then click the __Data Menu → Remove Duplicates__.
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/6832e010-a938-4490-9eb7-ce74ba6874ff" />

---

- Since the number of departments is still relatively small, I would like to try entering the data list manually into the source. However, if there is a large amount of data, it is permissible to use a source from a new sheet containing a list from which duplicates have been removed.
- Choose column B:B is the __Department__ column to be validated using __Data Validation__
- Open the __Data menu → Data Validation__
- Select __“Allow: List”__
- Select __"Source: IT;Marketing;Finance;HR;Sales"__
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/20318ca9-53a4-4a27-8ee2-81c5dff30a1c" />

---

6️⃣
- Choose column C:C is the __Age__ column to be validated using __Data Validation__
- Open the __Data menu → Data Validation__
- Select __"Input Message"__
- Give the title name: __Age Restriction__ and message: __"Please enter age between 18 and 65."__
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/6dd5dde4-a725-4d57-b24f-052816bdb4a8" />

---

7️⃣
- Choose column D:D is the __Salary($)__ column to be validated using __Data Validation__
- Open the __Data menu → Data Validation__
- Select __"Errort Alert"__
- Give the title name: __Invalid Salary__ and error message: __"Salary must be between 30,000 and 200,000."__
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/6e44eae3-cb95-4d9f-8f44-c35f12ce977f" />


***

### <div align="center">Results Overview</ins></div>


