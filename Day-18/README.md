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
1. Use XLOOKUP to find the assigned doctor for a given Patient ID.
2. Use XLOOKUP to find the Health Plan for a given Patient.
3. Use XLOOKUP to return Consultation Fee based on the plan.
4. Use XLOOKUP to return Free Checkup frequency.
5. BONUS: Add a dropdown for selecting Patient ID dynamically.

***

### <div align="center">Solving Step or Analysis</ins></div>
- To make today's work easier, I tried to create the display below to fill in the exercises to be done, as if the image below were a patient's paper in a medical clinic.
<div align="center"><img width="630" height="526" alt="image" src="https://github.com/user-attachments/assets/799dda70-9934-4d99-aafd-4def10e00236" /></ins></div>

---
- Create a list for __Patient ID__ by taking data from the __Appointments__ sheet with the source:

````excel
        =Appointments!$A$2:$A$363
 ````
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/c5a552b7-acdd-415e-b856-cc7cd63c1658" />

---

<img width="1920" height="1016" alt="image" src="https://github.com/user-attachments/assets/a2c78e03-41bf-4c8d-8821-bcdc68bb1bf9" />
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/8627f37e-3a23-4de9-9835-62a11a365b4b" />

---

<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/de99200e-a349-447b-93cf-28cf7e587c9d" />


***

### <div align="center">Results Overview</ins></div>
