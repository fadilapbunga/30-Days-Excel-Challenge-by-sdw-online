# 1️⃣8️⃣ Day 18: XLOOKUP

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

### ‼️‼️ __SINCE MY DEVICE DOES NOT SUPPORT HLOOKUP (EXCEL 2010), I WILL COMPLETE THIS EXERCISE USING A COMBINATION OF VLOOKUP AND INDEX MATCH__ ‼️‼️

***

### <div align="center">Identification Database</ins></div>
At a medical clinic, there are two datasets as shown in the images below:
<div align="center"><img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/70b2f8c3-9bad-4bcd-97b4-363b84307431" /></ins></div>
<div align="center"><img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/62a914e5-aa41-4b2d-bf57-b94eb50c0613" /></ins></div>


***

### <div align="center">Identification Issues</ins></div>
🏥 Scenario: Medical Clinic – Patient Scheduling & Health Plans
You're working as a data analyst for a health clinic. Your job is to pull useful patient and coverage information using XLOOKUP.

✅ __Dataset 1 (Sheet: Appointments):__
- List of scheduled patient appointments
- Fields: Patient ID, Patient Name, Appointment Date, Assigned Doctor, Department, Health Plan

✅ __Dataset 2 (Sheet: HealthPlanCoverage):__
- Horizontal table showing benefits under each health plan
- Rows: Consultation Fee, Lab Tests, Free Checkups
- Columns: Basic, Standard, Premium

📌 __Tasks:__

1️⃣ Use XLOOKUP to find the assigned doctor for a given Patient ID.

2️⃣ Use XLOOKUP to find the Health Plan for a given Patient.

3️⃣ Use XLOOKUP to return Consultation Fee based on the plan.

4️⃣ Use XLOOKUP to return Free Checkup frequency.

5️⃣ BONUS: Add a dropdown for selecting Patient ID dynamically.

***

### <div align="center">Solving Step or Analysis</ins></div>
- To make today's work easier, I tried to create the display below to fill in the exercises to be done, as if the image below were a patient's paper in a medical clinic.
<div align="center"><img width="630" height="526" alt="image" src="https://github.com/user-attachments/assets/799dda70-9934-4d99-aafd-4def10e00236" /></ins></div>

---


1️⃣
- To find the __Assigned Doctor__ based on the __Patient ID__, use the __=VLOOKUP__ formula as shown below, where the __lookup_value is the Patient ID row itself, the table_array is Table1 in the Appointments sheet, and the col_index_num is 4__ because the __Assigned Doctor__ is in row 4.

````excel
        =VLOOKUP($D$6;Table1;4;FALSE)
 ````

<div align="center"><img width="1920" height="1016" alt="image" src="https://github.com/user-attachments/assets/a2c78e03-41bf-4c8d-8821-bcdc68bb1bf9" /></ins></div>

---

- And to fill in the __Doctor's Department__, use the __=VLOOKUP__ formula as shown below, where the __lookup_value is the Doctor's Department row itself, the table_array is Table1 in the Appointments sheet, and the col_index_num is 5__ because the __Doctor's Department__ is in row 5.

````excel
        =VLOOKUP($D$6;Table1;5;FALSE)
 ````
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/8627f37e-3a23-4de9-9835-62a11a365b4b" /></ins></div>

---

2️⃣
- To find the __Health Plan__ based on the __Patient ID__, use the __=VLOOKUP__ formula as shown below, where the __lookup_value is the Patient ID row itself, the table_array is Table1 in the Appointments sheet, and the col_index_num is 6__ because the __Health Plan__ is in row 6.

````excel
        =VLOOKUP($D$6;Table1;6;FALSE)
 ````
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/de99200e-a349-447b-93cf-28cf7e587c9d" />

---

- To find the __Patient Name__, this time let's use a combination of the __INDEX MATCH__ formula as shown below:
- Determine the lookup value → __Patient Name__ on the __Appointments Sheet__
- Set the reference data range in the __Appointments Sheet__
- Fill in the __Patient Name__ column with the __INDEX + MATCH__ formula:

````excel
        =INDEX(Table1[Patient Name];MATCH(Sheet1!$D$6;Table1[Patient ID];0))
 ````
<img width="1920" height="1016" alt="image" src="https://github.com/user-attachments/assets/016e07ec-5509-4199-8a6f-4e8c0dd44f2b" />

---

- To find the __Appointment Date__, this time let's use a combination of the __INDEX MATCH__ formula as shown below:
- Determine the lookup value → __Appointment Date__ on the __Appointments Sheet__
- Set the reference data range in the __Appointments Sheet__
- Fill in the __Appointment Date__ column with the __INDEX + MATCH__ formula:

````excel
        =INDEX(Table1[Appointment Date];MATCH(Sheet1!$D$6;Table1[Patient ID];0))
 ````
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/9958f771-4f50-4320-9b7a-bb85981be7d6" />

---

3️⃣️
- To find the __Consultation Fee__, this time let's use a combination of the __INDEX MATCH__ formula as shown below:
- Determine the lookup value → __Consultation Fee__ on the __HealthPlanCoverage Sheet__
- Set the reference data range in the __HealthPlanCoverage Sheet__
- Fill in the __Consultation Fee__ column with the __INDEX + MATCH__ formula:

````excel
        =INDEX(HealthPlanCoverage!$B$2:$D$4;MATCH($B$15;HealthPlanCoverage!$A$2:$A$4;0);MATCH(Sheet1!$C$12;HealthPlanCoverage!$B$1:$D$1;0))
 ````
<img width="1920" height="1016" alt="image" src="https://github.com/user-attachments/assets/1fee1dde-3134-45ee-8002-20e21408036a" />

---

4️⃣
- To find the __Free Checkups__, this time let's use a combination of the __INDEX MATCH__ formula as shown below:
- Determine the lookup value → __Free Checkups__ on the __HealthPlanCoverage Sheet__
- Set the reference data range in the __HealthPlanCoverage Sheet__
- Fill in the __Free Checkups__ column with the __INDEX + MATCH__ formula:

````excel
        =INDEX(HealthPlanCoverage!$B$2:$D$4;MATCH(Sheet1!$B$16;HealthPlanCoverage!$A$2:$A$4;0);MATCH(Sheet1!$C$12;HealthPlanCoverage!$B$1:$D$1;0))
 ````

<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/75662dad-b4cb-4b65-a65f-fafe87f66d28" />

---

5️⃣ __BONUS__
- Create a list for __Patient ID__ by taking data from the __Appointments__ sheet with the source:

````excel
        =Appointments!$A$2:$A$363
 ````
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/c5a552b7-acdd-415e-b856-cc7cd63c1658" />
<img width="1920" height="1022" alt="image" src="https://github.com/user-attachments/assets/9e05a652-a034-41a1-a7fe-84a0101b1beb" />


***

### <div align="center">Results Overview</ins></div>
On Day 18: XLOOKUP challenge, I successfully built a patient data lookup system using a combination of __VLOOKUP and INDEX+MATCH__ as an alternative to XLOOKUP, which is not available in Excel 2010. The final result is a dynamic lookup form that displays complete patient information (name, visit date, doctor, department, health plan, consultation fee, and free checkups) based on the Patient ID selected via a dropdown menu.

