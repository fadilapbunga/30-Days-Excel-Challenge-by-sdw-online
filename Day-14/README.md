# 1️⃣4️⃣ Day 14: Practice (Week 2 review)

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

### <div align="center">Identification Database</ins></div>
There are over 2500 pieces of data from a retail tech company consisting of __Order ID, Customer Name, Product, Quantity, Order Date, Delivery Date, Price ($), and Email__ columns.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/bb7a59f3-058f-431e-8ff2-30831690c120" />

***

### <div align="center">Identification Issues</ins></div>
__Your task:__
You are working for a retail tech company, and your team has received a file with 2,500+ orders.
You need to clean this dataset to ensure no invalid or suspicious data enters the system.

__Tasks:__

1️⃣ Apply data validation to the following columns:

  ➤ Order ID: Whole numbers between 1000 and 9999
  
  ➤ Quantity: Must be between 1 and 10
  
  ➤ Order Date: Cannot be a future date
  
  ➤ Delivery Date: Must be at least one day after the order date
  
  ➤ Price: Must be between $100 and $20,000
  
  ➤ Email: Must contain '@' and '.'

2️⃣ Create a dropdown list for products so users can only select valid items

3️⃣ Add an input message for the Quantity column

4️⃣ Add a custom error message if someone enters an invalid price

__Goal:__
Use data validation to improve data quality and prevent future errors in reporting.

***

### <div align="center">Solving Step or Analysis</ins></div>

1️⃣
- Choose column A:A is the __Order ID__ column to be validated using __Data Validation__
- Open the __Data menu → Data Validation__
- Select __“Allow: Whole Number”__
- Select __"Data between 1000 and 9999"__
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/43bb621e-8120-41eb-80b9-e6738d547647" />

---

- Choose column D:D is the __Quantity__ column to be validated using __Data Validation__
- Open the __Data menu → Data Validation__
- Select __“Allow: Whole Number”__
- Select __"Data between 1 and 10"__
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/26124cfb-f5cb-45f8-b81c-87446e275c87" />

---

- Choose column E:E is the __Start Date__ column to be validated using __Data Validation__
- Open the __Data menu → Data Validation__
- Select __“Allow: Date”__
- Select __"Data between Start Date: 2020-01-01 and End Date: =TODAY()"__
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/7c5c107b-b112-479e-bb9c-6abd719d353f" />

---

- Choose column F:F is the __Email__ column to be validated using __Data Validation__
- Open the __Data menu → Data Validation__
- Select __“Allow: Custom”__
- Enter the following formula:

````excel
		=F2>=E2+1
 ````

<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/a223afff-ec1e-400c-9b04-49032faf841c" />

---

- Choose column G:G is the __Price($)__ column to be validated using __Data Validation__
- Open the __Data menu → Data Validation__
- Select __“Allow: Whole Number”__
- Select __"Data between $100 and $20000"__
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/cf83621e-95e4-4746-a5a1-f372ac84cff4" />

---

- Choose column H:H is the __Email__ column to be validated using __Data Validation__
- Open the __Data menu → Data Validation__
- Select __“Allow: Custom”__
- Enter the following formula:

````excel
		=AND(ISNUMBER(SEARCH("@";H2)); ISNUMBER(SEARCH(".";H2)))
 ````
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/c93f529c-cb26-4c13-85cc-94b55df760f8" />

---

2️⃣

- Take the list of unique product names by copying the list of product names to a new sheet called __list_of_product__.
- Open the __Data menu → Remove Duplicates__
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/6699fc34-8cad-4091-9f00-76233f3a0222" />

---

- Choose column C:C is the __Product__ column to be validated using __Data Validation__
- Open the __Data menu → Data Validation__
- Select __“Allow: Custom”__
- Enter the following formula:

````excel
		=list_of_product!$A$2:$A$9
 ````

<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/2e3c793e-e819-4a22-8686-3175922eec8f" />

---

3️⃣

- Choose column D:D is the __Quantity__ column to be validated using __Data Validation__
- Open the __Data menu → Data Validation__
- Select __"Input Message"__
- Give the title name: __Number of Quantity__ and message: __"Please enter quantity between 1 and 10."__
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/31073246-ea8d-4d84-9f56-ca73b943db1b" />

---

4️⃣

- Choose column G:G is the __Price($)__ column to be validated using __Data Validation__
- Open the __Data menu → Data Validation__
- Select __"Errort Alert"__
- Give the title name: __Invalid Price__ and error message: __"Price must be between $100 and $20000."__
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/f765f6c7-2c9a-4629-b394-18445d3860b6" />


***

### <div align="center">Results Overview</ins></div>

1️⃣

- To ensure that data validation has been applied correctly, I tried entering an __Order ID of 10000__, which is outside the requirements, and the result was __“The value doesn't match the data validation restrictions defined for this cell.”__ And the result is a warning that we must enter a number within the requested range.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/98728053-9b50-4e3e-89a0-bcf2c2b1423f" />

---

- To ensure that data validation has been applied correctly, I tried entering an __Quantity of 11__, which is outside the requirements, and the result was __“The value doesn't match the data validation restrictions defined for this cell.”__ And the result is __a warning__ that we must enter a quantity within the requested range.
<img width="1920" height="1016" alt="image" src="https://github.com/user-attachments/assets/14efdbb7-2d25-4db2-8cf4-8bd0a683115e" />

---

- To ensure that data validation has been applied correctly, I tried entering a date that is __tomorrow or later than today, namely 11/14/2025.__ The result shows that __“The value doesn't match the data validation restrictions defined for this cell".__ This means that data validation is working correctly according to the specified conditions.
<img width="1920" height="1016" alt="image" src="https://github.com/user-attachments/assets/9b3fcaac-4a93-47bd-8182-5276019deb44" />

---

- To ensure that data validation has been applied correctly, I tried entering a date that is __same as today, namely 11/13/2025__. The result shows that __“The value doesn't match the data validation restrictions defined for this cell".__ This means that data validation is working correctly according to the specified conditions must be at least one day after the order date.
<img width="1920" height="1016" alt="image" src="https://github.com/user-attachments/assets/4150c51b-22cb-419c-912d-7522691a694b" />

---

- To ensure that data validation has been applied correctly, here I try to enter __a price of 99__, which is outside the requirements, and the result is a warning that we must enter a salary within the requested range.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/2783174e-d419-4cb5-81db-f4c24a5e26a5" />

---

- To ensure that data validation has been applied correctly, here I try to enter only the name __“bunga@”__. With one of the characters that is a requirement, it turns out that the data doesn't match and __must contain 2 characters__.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/8fd2c566-67dc-486b-88b5-0d8305a5fc45" />

---

2️⃣

- When selecting a product, there is a __Dropdown List from Data Validation__ that can be selected to avoid entering products outside the list.
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/9a2fd7ca-5cb8-4577-b30f-fe0bcddb1531" />

---









