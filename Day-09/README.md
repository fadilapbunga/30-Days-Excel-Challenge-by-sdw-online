# 9️⃣ Day 9: Text functions

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

### Identification Database 
To practice this function, it consists of data with messy writing formats as shown in the image below.
<img width="960" height="509" alt="image" src="https://github.com/user-attachments/assets/c665840f-8e2d-4da4-8935-9f53bff12ad1" />

***

### Identification Issues
Today’s challenge is to clean and transform messy text data using Excel’s text functions.
You’ll work with customer orders and apply formulas to make the data clean, structured, and ready for analysis.

✅ __Task 1: Clean the Order ID__

Use =UPPER(A2) to make all Order IDs uppercase.

✅ __Task 2: Standardize Customer Names__

Use =PROPER(B2) to format names like "jOHN sMITH" into "John Smith"

✅ __Task 3: Trim Product Names__

Use =TRIM(C2) to remove unwanted spaces.

✅ __Task 4: Extract Product Code Details__

Use =MID(E2,5,LEN(E2)-4) to extract the unique product ID after "PRD-".

✅ __Task 5: Split Full Name into First and Last Name__

First Name: =LEFT(B2, FIND(" ", B2)-1)
Last Name: =IF(ISNUMBER(FIND(" ", B2)), RIGHT(B2, LEN(B2)-FIND(" ", B2)), "No Last Name")

✅ __Task 6: Count Product Name Length__

Use =LEN(C2) to count number of characters in each product name.

🎨 __BONUS – Add Conditional Formatting__

- Yellow Fill: Quantity >= 3
- Red Fill: Customers with "No Last Name"

✅ Now turn your cleaned columns into a structured table.
Sort or filter to analyze the data efficiently.

***

### Solving Step or Analysis

✅ __Task 1: Clean the Order ID__

- Even though the order IDs in the data appear to be all uppercase, to ensure that all letters are in uppercase format, use __=UPPER__ to standardize the format of the order IDs to uppercase letters.
<img width="1920" height="1017" alt="image" src="https://github.com/user-attachments/assets/f1a4bfc8-d9cb-4fb6-9683-2a7b53d40140" />

***

✅ __Task 2: Standardize Customer Names__

- Same as the order ID column, ensure that the text is written neatly by making sure that each letter starts with a capital letter followed by a lowercase letter using __=PROPER__.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/f0eb1fca-b130-47d3-a3b7-f578aaa7ff85" />

***

✅ __Task 3: Trim Product Names__

- The data in the product name column looks messy and contains many unnecessary spaces, so the first thing to do is to remove the excess spaces using the __=TRIM__ formula. Then, to make the text look neater, use the __=PROPER__ formula so that the first letter is capitalized and followed by lowercase letters.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/f4e49a4d-41ab-4432-90ce-190032ec65e6" />
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/287210da-8870-418d-aa05-860a2f7d5778" />

***

✅ __Task 4: Extract Product Code Details__

- Taking the name after PRD—you can use several alternatives. For the first one, you can use a combined formula between __=MID__ and __=LEN__ if the number of characters in the product code column varies. To combine the two formulas, the formula is:
````excel
		=MID($E2;5;LEN($E2)-4)
 ````
- Where, the text to be taken is in column E, character retrieval starts from the 5th letter, and the number of characters to be taken is the total number of combined characters minus 4 because “PRD-” consists of 4 characters and we want to take the characters after that.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/e2333ab0-7d48-4c6e-9b2b-e99d6628428d" />

- However, if all the characters in the product code column have the same number and are constant, another alternative is to use the __=RIGHT__ formula to extract characters from the right, as shown in the following formula and image. There are 5 characters to be taken from the right.
````excel
		=RIGHT($L2;5)
 ````
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/512e23f1-b5ca-4482-8d77-6586d53f7877" />

***

✅ __Task 5: Split Full Name into First and Last Name__

- To extract the first name, use a combination of the __=LEFT__ and __=FIND__ functions, where the first name is taken from the left side of the text with its character number. If a space __“ ”__ is found in the text, take the character before the space or write __“-1”__. However, if someone does not have a last name, the value is returned to the text in that column using the __=IFERROR__ function.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/7d805765-1292-455a-a624-20b3d88f2b73" />

- To extract the last name, use three combined formulas: __RIGHT, LEN, and FIND__. This extracts the last name starting from the right with num_chars being the total number of characters minus any characters encountered if they are spaces or __“ ”__, meaning that character extraction from the right will stop if a space is found in the characters. If someone does not have a last name, then the column will be written as __“No Last Name”__ using the __=IFERROR__ formula.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/7e7511c0-f782-43c4-acea-5d3b4c3d3399" />

***

✅ __Task 6: Count Product Name Length__

- Use __=LEN($J2)__ to count number of characters in each product name.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/1c5254d7-c7ad-4fda-877b-4c2eca518e6f" />

***

🎨 __BONUS – Add Conditional Formatting__

- Use conditional formatting by giving a yellow fill color to quantities greater than or equal to 3.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/a7444874-57c7-4691-a950-7088b14b72f2" />
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/f28bf071-68d1-43b8-9112-1e5ca4781920" />

***

- Use conditional formatting by giving a red fill color to someone who does not have a last name.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/d614e20d-09f3-463c-8dd0-38e32af64613" />
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/a04a4cfd-6358-419e-8359-dd4252d34e0b" />


### Results Overview

Based on the analysis of the above data using filters or sorting, there are:
- Using the __UPPERCASE__ formula in the Order ID column capitalizes all letters.
- Using the __PROPER__ formula makes the data neater and more proper by capitalizing the first letter of each word followed by lowercase letters, as in the Customer Name column.
- Successfully trimmed excess spaces using the __TRIM__ formula in the Product Name column and made the data look better by combining it with the __PROPER__ formula.
- Extracting characters from the product code column and taking only the last 5 characters can be done using several alternatives. The first is to combine the __MID__ and __LEN__ formulas, and the second is to use the __RIGHT__ formula if the characters are constant or the number of characters and the characters to be taken are the same.
- Take the first name using a combination of the __LEFT__ and __FIND__ formulas, and if an error is found because there are customers who do not have a long name, use the __IFERROR__ formula. Similarly, take the last name successfully extracted by combining three formulas, namely __RIGHT__, __LEN__, and __FIND__. And for customers who do not have a long name, give the description “No Last Name”.
- Calculate the total number of characters in the product name using the __LEN__ formula.
- Using __Conditional Formatting__, we get the result that: 256 data points with a quantity greater than 3, 37 people who do not have a last name, and there are 30 data points that have a quantity greater than 3 and do not have a last name/both.

***
