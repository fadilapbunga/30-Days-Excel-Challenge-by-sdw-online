# 4️⃣ Day 4: Sorting and filtering data

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

## Identification Database
The workbook is about an online course sales across different regions and months. And it has variety of columns like Month, Course, Region, Sales, Expenses, Profit as many as 200 lines in Dollar US. Below, the workbook table contains approximately three examples of initial data. 

| Month |    Course     | Region | Sales ($) | Expenses ($) | Profit ($) |
| ----- | ------------- | ------ | --------- | ------------ | ---------- |
| Oct   | AI Prompting  | East   | 2555      | 1805         | 750        |
| Aug   | Data Cleaning | West   | 5085      | 3027         | 2058       |
| Aug   | Phyton Basics | North  | 4221      | 4640         | -419       |
| ...   | ............. | ....   | ....      | ....         | ....       |


***

## Identification Issues
1. Sort by Sales ($) from highest to lowest.
2. Sort by Profit ($), then by Month alphabetically.
3. Filter to show only rows with:
   - Sales greater than $6000
   - Profit between $1000 and $3000
   - Region is 'North' or 'West'
4. Create a new column: 'Profit Margin' = Profit ($) / Sales ($)
   - Use filtering to find the lowest margin.
   - Use sorting to find the highest margin.

***

## Solving Step or Analysis
1. Sort Sales ($) from the highest to lowest, using Sort and Filter features at Editing. It turns out in September with Power BI Course at South Region have the highest sales with $6962 and in Feb with AI Prompting at South Region have the lowest sales with $1042.

<img width="1924" height="1016" alt="Image" src="https://github.com/user-attachments/assets/adf6e3b7-b900-4716-9a2c-042e146b49b3" />
<img width="960" height="494" alt="Image" src="https://github.com/user-attachments/assets/a5047155-9e63-4648-9e71-d3b2c5a7b2fe" />

***

2. Sort the values with 2 condition using Custom Sort, first by Profit ($) from the highest to lowest and the second by Month alphabetically. The result proves that this order is correct. Look at the second image below. There are profit values that are the same, namely 5150 in August and May, but both come from different courses and regions. In terms of month alphabetically, the profit value in August is in first place after May.

<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/e13a99b4-840f-4d3a-ac67-e5dcc6846b63" />
<img width="1920" height="1017" alt="image" src="https://github.com/user-attachments/assets/e9a29846-8041-4fef-84cd-074684c5723e" />

***

3.
- To show Sales greater than $6000, use Custom Sort and choose 'Greater Than' and add value 6000 like the picture below.
<img width="1924" height="1080" alt="image" src="https://github.com/user-attachments/assets/df58b0ef-b6fa-4cf6-a04e-ba722803d857" />

- To show Profit between $1000 and $3000, use Custom Sort and choose 'Greater Than' and add value $1000 is greater than $3000, and less than $3000.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/4bafc79e-8709-479c-a677-3a8c41020dd6" />

- To show only 'North' or 'West' region, use filters and only se;ect the sections you want to display like the picture below.
<img width="1922" height="1018" alt="image" src="https://github.com/user-attachments/assets/f17cf984-cc15-43c6-8038-ead579c8eb58" />

And the image below is the result of sorting and filtering.
<img width="960" height="509" alt="image" src="https://github.com/user-attachments/assets/f0b1ff53-0e49-4013-8b95-e0b02ddf6c60" />

***

4.
- Create column 'Profit Margin' with formula: Profit($) / Sales($)
<img width="1922" height="1022" alt="image" src="https://github.com/user-attachments/assets/3d69e921-78c9-4483-a8dd-4d89302e7354" />

- Use filter to sort Profit Margin from the lowest into highest. And the result is at the second picture. The lowest Profit Margin is -3,81 in Feb by AI Prompting course, South Region.
<img width="1918" height="1018" alt="image" src="https://github.com/user-attachments/assets/81a5a9be-cecf-4e26-818e-af6a50c2dc08" />
<img width="960" height="509" alt="image" src="https://github.com/user-attachments/assets/c6f98cb6-e28c-4515-a5e3-573f23cab2a3" />

- Use sorting to find Profit Margin from the highest into lowest. And the result is at the second picture. The higest Profit Margin are 0,87 in April by Power BI course, West region and in May by AI Prompting course, South region.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/de3cb48e-57db-4a7b-a364-f8568d538e69" />
<img width="960" height="508" alt="image" src="https://github.com/user-attachments/assets/db2309b4-75f7-4199-95ce-6b2158b1fe6e" />


***


## Results Overview
- 
