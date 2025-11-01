# 8️⃣ Day 8: Logical functions (IF/ELSE)

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

### Identification Database
There is a dataset from a university's admin team and we were asked to help them assess student progress by applying logical formulas. The dataset is at 'Student Performance' sheet. It contains Student ID,	Name,	Course,	Attendance (%),	Test Score,	Final Exam Score,	Pass Status,	Grade Category, and	Intervention Flag. Like the picture below:
<img width="959" height="508" alt="image" src="https://github.com/user-attachments/assets/b4a730b0-45fc-46b1-b17b-488ee73a913d" />

***

### Identification Issues
There are 3 tasks that must be completed.

✅ __Task 1 – Determine Pass Status__

✅ __Task 2 – Assign Grade Category__
Use the IFS function with these rules:
- Score >= 85 → 'Distinction'
- Score >= 60 → 'Pass'
- Score < 60 → 'Fail'

✅ __Task 3 – Flag Students Needing Intervention__
Use IF with AND/OR:
Flag students as needing intervention if:
- Attendance is less than 75% OR Final Exam Score is less than 50


📌 __BONUS:__
1. Use Conditional Formatting on 'Intervention Flag':
   - Red Fill for 'Needs Intervention'
   - Green Fill for 'OK'
2. Sort the dataset so that flagged students appear at the top

***

### Solving Step or Analysis

✅ __Task 1 – Determine Pass Status__

- To determine pass status, there are two conditions, namely ‘pass’ or ‘fail’, with the condition that if the final exam score is greater than or equal to 50, then the pass status is pass, and if it does not meet this condition, then the status is fail. We write the formula as below:

````excel
		=IF($F2>=50;"Pass";"Fail")
 ````
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/49213360-f77d-44ed-8067-c06831600c24" />

***

✅ __Task 2 – Assign Grade Category__

- To assign 'Grade Category', there are three conditions: ‘distinction’ for a final exam score of 85 or higher, ‘pass’ for a final exam score of 60 or higher, and ‘fail’ for a final exam score of less than 60. Here, I am trying to use nested __=IF__ formulas, not IFS. Both can be used and will produce the same output. Both formulas can be broken down as follows:

````excel
		=IF($F2>=85;"Distinction";IF($F2>=60;"Pass";"Fail"))
 ````
or

````excel
		=IFS($F2>=85;"Distinction";$F2>=60;"Pass";$F2<60;"Fail")
 ````
<img width="1920" height="1017" alt="image" src="https://github.com/user-attachments/assets/9255f6f6-1d61-4317-bec4-8233189a9aee" />


***


✅ __Task 3 – Flag Students Needing Intervention__

- For task 3, there are several conditions that require the use of two functions in one command. The functions used are __=IF__ and __=OR__. If both conditions are met, then Intervention is needed, and vice versa.

````excel
		=IF(OR($D2<75%;$F2<50);"Needs Intervention";"OK")
 ````

<img width="1909" height="1000" alt="image" src="https://github.com/user-attachments/assets/45a37eb9-f879-4096-8041-9e9b4c320d6d" />


***

📌 __BONUS:__

__1.__ Use conditional formatting with two rules, namely equal to, then change the fill color according to the command.
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/123556db-b40c-41f2-a03d-868a86b155fc" />

__2.__ And for this sort, use a custom sort based on cell color. We want to know that the top row only contains students who need intervention, so change the custom sort to red cells and place them on top. .              
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/108ffc93-7f1d-447f-9b32-442bbfac8d49" />


***


### Results Overview
- Initially, there were many students with Fail status who needed intervention, indicating poor academic performance.
- After applying IF and IFS logic, it was found that most students with a Final Exam Score ≥ 50 passed and did not need intervention.
- Students with a score ≥ 85 were categorized as Distinction, indicating excellent academic performance.
- The Intervention Flag feature is effective in helping the academic team identify students who need special attention (attendance < 75% or score < 50).
- Overall, Excel logic helps create an efficient and easy-to-understand automated grading system.
