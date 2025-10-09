# 1️⃣ Day 1: Getting started with Excel

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

## Identification Database
The table below shows performance data for 5 online courses.
| Course Name        | Instructor | Registered Students | Completed Students
| ---------------    | ---------- | ------------------- | ----------------- | 
| Intro to Python    | Alex       | 120                 | 100               |
| Excel for Business | Nina       | 95                  | 80                |
| SQL Bootcamp       | Chris      | 140                 | 125               |
| Data Visualization | Taylor     | 85                  | 75                |
| Power BI Mastery   | Jordan     | 110                 | 98                |		
			

***

## Identification Issues
- Use a formula to calculate the completion rate (as a percentage).
- Explore the formula bar, ribbon tabs (Home, Formulas, Insert), and name box.
- Try adding a new row for a course of your choice and calculate its completion rate.
- Optional: Format the table to improve readability (bold headers, borders, etc).


***

## Solving Step or Analysis
1. Since we know how much are the number of Registered and Completed Students, formula to calculate the completion rate(%) for the table below, we can using: 
  ````excel
		(Completed Students / Registered Students) x 100% 
 ````
Which is we can write the formula above on formula bar where the completion rate column is
<img width="739" height="448" alt="Image" src="https://github.com/user-attachments/assets/bc7b9d36-e89d-4a40-b200-7616cbf59e5d" />

For example, based on the image above, Completion Rate column is in column E. So we can click Formula on Ribbon Tabs and then click Insert Formula on E7 and write down the formula on Formula Bar like =$D7/$C7 since Registered and Completed Students column on C and D. And since the Microsoft Excel has extensive features for working with percentages, we can turn the number result by click the Percent Styles to format as a percent.

2. To explore more the using of Microsoft Excel, we can turn the data into table format using Tables features on Insert. And we can give the name of table by Name Box on the top left into data_online_courses.
<img width="1365" height="894" alt="Image" src="https://github.com/user-attachments/assets/4fecf049-0a81-437d-8aa5-ecc9fa5b90f0" />
<img width="960" height="512" alt="Image" src="https://github.com/user-attachments/assets/4b9a0fef-f5dc-4326-aeda-3da30f46d92e" />


3. To sharpen knowledge on the first day, i try it again with the different numbers at new sheet and even i add Data Bars in Conditional Formatting.

<img width="539" height="496" alt="Image" src="https://github.com/user-attachments/assets/617a2cdd-825a-4c84-9cc9-b78b090a4d5d" />

***


## Results Overview
| Course Name        | Instructor | Registered Students | Completed Students| Completion Rate (%) 
| ---------------    | ---------- | ------------------- | ----------------- | -------------------
| Intro to Python    | Alex       | 120                 | 100               | 83%
| Excel for Business | Nina       | 95                  | 80                |84%
| SQL Bootcamp       | Chris      | 140                 | 125               |89%
| Data Visualization | Taylor     | 85                  | 75                |88%
| Power BI Mastery   | Jordan     | 110                 | 98                |	89%

The classes with the highest completion rates are SQL Bootcamp and Power BI Mastery, each with a completion rate of 89%.
