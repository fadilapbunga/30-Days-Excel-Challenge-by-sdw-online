# 9️⃣ Day 9: Text functions

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

## Identification Database
To practice this function, it consists of data with messy writing formats as shown in the image below.
<img width="960" height="509" alt="image" src="https://github.com/user-attachments/assets/c665840f-8e2d-4da4-8935-9f53bff12ad1" />

***

## Identification Issues
Today’s challenge is to clean and transform messy text data using Excel’s text functions.
You’ll work with customer orders and apply formulas to make the data clean, structured, and ready for analysis.

✅ Task 1: Clean the Order ID
Use =UPPER(A2) to make all Order IDs uppercase.

✅ Task 2: Standardize Customer Names
Use =PROPER(B2) to format names like "jOHN sMITH" into "John Smith"

✅ Task 3: Trim Product Names
Use =TRIM(C2) to remove unwanted spaces.

✅ Task 4: Extract Product Code Details
Use =MID(E2,5,LEN(E2)-4) to extract the unique product ID after "PRD-".

✅ Task 5: Split Full Name into First and Last Name
First Name: =LEFT(B2, FIND(" ", B2)-1)
Last Name: =IF(ISNUMBER(FIND(" ", B2)), RIGHT(B2, LEN(B2)-FIND(" ", B2)), "No Last Name")

✅ Task 6: Count Product Name Length
Use =LEN(C2) to count number of characters in each product name.

🎨 BONUS – Add Conditional Formatting
- Yellow Fill: Quantity >= 3
- Red Fill: Customers with "No Last Name"

✅ Now turn your cleaned columns into a structured table.
Sort or filter to analyze the data efficiently.

***

## Solving Step or Analysis

✅ Task 1: Clean the Order ID

- Even though the order IDs in the data appear to be all uppercase, to ensure that all letters are in uppercase format, use =UPPER to standardize the format of the order IDs to uppercase letters.
<img width="1920" height="1017" alt="image" src="https://github.com/user-attachments/assets/f1a4bfc8-d9cb-4fb6-9683-2a7b53d40140" />

***

✅ Task 2: Standardize Customer Names

- Same as the order ID column, ensure that the text is written neatly by making sure that each letter starts with a capital letter followed by a lowercase letter using =PROPER.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/f0eb1fca-b130-47d3-a3b7-f578aaa7ff85" />

***

✅ Task 3: Trim Product Names

- The data in the product name column looks messy and contains many unnecessary spaces, so the first thing to do is to remove the excess spaces using the =TRIM formula. Then, to make the text look neater, use the =PROPER formula so that the first letter is capitalized and followed by lowercase letters.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/f4e49a4d-41ab-4432-90ce-190032ec65e6" />
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/287210da-8870-418d-aa05-860a2f7d5778" />

***

✅ Task 4: Extract Product Code Details

- Taking the name after PRD—you can use several alternatives. For the first one, you can use a combined formula between mid and len if the number of characters in the product code column varies. To combine the two formulas, the formula is:
````excel
		=MID($E2;5;LEN($E2)-4)
 ````
- Where, the text to be taken is in column E, character retrieval starts from the 5th letter, and the number of characters to be taken is the total number of combined characters minus 4 because “PRD-” consists of 4 characters and we want to take the characters after that.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/e2333ab0-7d48-4c6e-9b2b-e99d6628428d" />

- However, if all the characters in the product code column have the same number and are constant, another alternative is to use the RIGHT formula to extract characters from the right, as shown in the following formula and image. There are 5 characters to be taken from the right.
````excel
		=RIGHT($L2;5)
 ````
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/512e23f1-b5ca-4482-8d77-6586d53f7877" />

***

✅ Task 5: Split Full Name into First and Last Name

- To extract the first name, use a combination of the LEFT and FIND functions, where the first name is taken from the left side of the text with its character number. If a space “ ” is found in the text, take the character before the space or write “-1”. However, if someone does not have a last name, the value is returned to the text in that column using the IFERROR function.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/7d805765-1292-455a-a624-20b3d88f2b73" />

- To extract the last name, use three combined formulas: RIGHT, LEN, and FIND. This extracts the last name starting from the right with num_chars being the total number of characters minus any characters encountered if they are spaces or “ ”, meaning that character extraction from the right will stop if a space is found in the characters. If someone does not have a last name, then the column will be written as “No Last Name” using the IFERROR formula.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/7e7511c0-f782-43c4-acea-5d3b4c3d3399" />

***

✅ Task 6: Count Product Name Length

- Use =LEN($J2) to count number of characters in each product name.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/1c5254d7-c7ad-4fda-877b-4c2eca518e6f" />

***

🎨 BONUS – Add Conditional Formatting

- Use conditional formatting by giving a yellow fill color to quantities greater than or equal to 3.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/a7444874-57c7-4691-a950-7088b14b72f2" />
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/f28bf071-68d1-43b8-9112-1e5ca4781920" />

***

- Use conditional formatting by giving a red fill color to someone who does not have a last name.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/d614e20d-09f3-463c-8dd0-38e32af64613" />
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/a04a4cfd-6358-419e-8359-dd4252d34e0b" />


## Results Overview

Based on the analysis of the above data using filters or sorting, there are:
- 256 data points with a quantity greater than 3
- 37 people who do not have a last name.
- And there are 30 data points that have a quantity greater than 3 and do not have a last name/both.

***
