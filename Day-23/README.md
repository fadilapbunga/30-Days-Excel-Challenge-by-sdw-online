# 2️⃣3️⃣ Day 23: Dynamic array functions

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

### <div align="center">Identification Database</ins></div>
📌 __Scenario:__  
You're helping an animal shelter in Canada analyze their adoption data.  
They want insights like common breeds, top-paying adopters, and more.  

✅ __Sheet: shelter_data__  
Columns include: Adoption ID, Animal Type,	Breed,	Age (Years),	Adoption Fee,	Adoption Date,	City,	Payment Method.
 <div align="center"><img width="1081" height="579" alt="image" src="https://github.com/user-attachments/assets/e3537da5-fee7-4162-a34b-3f46f5228dd4" /></ins></div>

***

### <div align="center">Identification Issues</ins></div>
🧪 __Tasks:__

1️⃣ List all unique animal types that were adopted.

2️⃣ Show the top 10 most expensive adoptions.

3️⃣ Filter for adoptions made in 'Toronto' using Credit Card.

4️⃣ Return the 15 most recent adoptions.

5️⃣ Extract only 'Animal Type' and 'Adoption Fee' columns.

6️⃣ Bonus: Use TAKE, DROP, CHOOSECOLS, CHOOSEROWS to create your own insights.

***

### <div align="center">Solving Step or Analysis</ins></div>

#### <div align="center">‼️ Due to environment constraints where dynamic array functions are not supported, all analysis was performed using Microsoft Excel in a non-dynamic array setting, leveraging Advanced Filter, sorting techniques, and foundational Excel functions to achieve accurate and reliable results.‼️</ins></div>

1️⃣
- To find unique names for all animal types, you can use the __=UNIQUE__ formula in a __dynamic array__. Use the formula below, with the array being the Animal Types column:
````excel
    = UNIQUE($B$1:$B$401)
 ````
---
- And for __a non-dynamic array__, the steps can be done as follows:  
▶️ Block the Animal Types column  
▶️ Select Advanced Filter  
▶️ Select Copy to another location  
▶️ Select the list range to be selected, which is in the Animal Types column, namely in the range $B$1:$B$401  
▶️ Select copy to $J$1 to move the temporary results  
▶️ And don't forget to check Unique Record Only


<div align="center"><img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/c60f5863-ab84-49e3-88c3-ab7ca6c4d2f4" /></ins></div>

<div align="center"><img width="611" height="199" alt="image" src="https://github.com/user-attachments/assets/54afad67-5262-4190-afe8-3579e4a6fea8" /></ins></div>

---
2️⃣
- To sort the most expensive adoptions, __a dynamic array__ can use the __=SORTBY__ formula, which sorts data based on specific criteria, as shown in the formula below:
````excel
    = SORTBY($A$1:$H:$401;$E:$E;-1)
 ````
▶️ Use the __=TAKE__ function to retrieve the top 10 data using the formula below, where row is __10__ because it is the first 10 from top to bottom, and column is __8__ because it is from left to right.
````excel
    = TAKE($A$1:$H:$401;10;8)
 ````
▶️ And from the two formulas, when combined, it becomes:
````excel
    = TAKE(SORTBY($A$1:$H:$401;$E:$E;-1);10;8))
 ````
---
- And for __a non-dynamic array__, the steps can be done as follows:  
▶️ Use the filter feature in the Adoption fee column header.  
▶️ Click Number filter.  
▶️ Then select Top 10.

<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/9b89f596-93eb-4be2-afa6-5787b516ea8e" /></ins></div>
<div align="center"><img width="1191" height="415" alt="image" src="https://github.com/user-attachments/assets/8eea0342-1fed-40de-8973-8a89ef05d1db" /></ins></div>
AND THEN PAKE RUMUS TAKE



---
3️⃣
- To filter with two __dynamic array__ criteria conditions, the __=FILTER__ function can be used by combining criteria __AND (*)__ logic as shown in the formula below:
````excel
    = FILTER($A$1:$H:$401; ($G$1:$G$401 = "Toronto") * ($H$1:$H$401 = "Credit Cash"); "No Data")
 ````
---
- And for __a non-dynamic array__, the steps can be done as follows:  
▶️ Filter the __City__ column by checking only the __"Toronto"__ section.
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/8be4b91a-6d15-4d44-86ee-98085936c575" /></ins></div>

▶️ Filter the __Payment Method__ column by checking only the __"Credit Cash"__ section
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/07ab4950-dae7-4791-b847-954140195d36" /></ins></div>
<div align="center"><img width="1191" height="489" alt="image" src="https://github.com/user-attachments/assets/7792b29e-d4af-4f61-825a-96e2f5db5fa0" /></ins></div>

---
4️⃣
- To return the most recent adoption in __a dynamic array__, the first step is to ensure that the adoption date __data has been filtered from newest to oldest__.
- Then take the 15 most recent data points using the __=TAKE__ formula as shown below, where row is __15__ because it is the first 15 from top to bottom, and column is __8__ because it is from left to right.
````excel
    = TAKE($A$1:$H:$401;15;8)
 ````
---
-  And for __a non-dynamic array__, the method is more or less the same. The key is to filter the Adoption Date column from Newest to Oldest and manually copy the top 15 data entries.
<div align="center"><img width="1920" height="1016" alt="image" src="https://github.com/user-attachments/assets/31b529a6-59c2-4d35-a6a8-48f9c5c4109f" /></ins></div>
<div align="center"><img width="1205" height="515" alt="image" src="https://github.com/user-attachments/assets/2caf968e-7fa9-4450-aad2-8f89c2a8adcd" /></ins></div>

---
5️⃣
- To __dynamically__ extract the ‘Animal Types’ and ‘Adoption Fee’ columns into an array, use the __=CHOOSECOL__ formula as shown below, where the ‘Animal Types’ column is in column 2 and ‘Adoption Fee’ is in column 5.
````excel
    = TAKE($A$1:$H:$401;2;5)
 ````
---
- To extract the 'Animal Type' and 'Adoption Cost' columns as __a non-dynamic array__, simply copy and paste the two columns.
<div align="center"><img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/a413ded1-6b8f-4398-b396-78d845f4315d" /></ins></div>
<div align="center"><img width="683" height="587" alt="image" src="https://github.com/user-attachments/assets/018e3896-21fc-4a29-afa6-4fd05483a67b" /></ins></div>

***

### <div align="center">Results Overview</ins></div>
This project demonstrates that complete and accurate data analysis can be achieved using fundamental Excel techniques, even without dynamic array support, highlighting strong problem-solving skills and adaptability to real-world tool limitations. Replicated modern Excel behaviors (FILTER, UNIQUE, TOP N) through legacy-compatible methods, ensuring analysis remained scalable and reliable.
