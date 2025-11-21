# 1️⃣7️⃣ Day 17: INDEX + MATCH

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

### <div align="center">Identification Database</ins></div>
There is a dataset from Customer Support Ticket Management, and here, as a Support Operations Analyst, we are expected to manage daily support activities.

✅ __Dataset 1 (Sheet: SupportTickets):__
- Records of support tickets raised by customers
- Fields: Ticket ID, Customer Name, Issue Type, Assigned Agent, Department, Priority
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/2c1c5c3d-8f7c-4b59-9a9d-ddc33c24a6b7" /></ins></div>


✅ __Dataset 2 (Sheet: AgentAvailability):__
- Weekly schedule showing available hours, ticket capacity, and on-call status by day
<div align="center"><img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/a284f2f3-043c-43fb-993f-04d9a38fc2e9" /></ins></div>


***

### <div align="center">Identification Issues</ins></div>

✅ __Tasks:__
1. Use INDEX-MATCH to find the Assigned Agent for a given Ticket ID.
2. Use INDEX-MATCH to find the Priority of a given Ticket.
3. Use INDEX-MATCH to look up Available Hours for a specific weekday.
4. Use INDEX-MATCH to check if the agent is On Call that day.
5. BONUS: Add a dropdown for Ticket ID to drive the lookup dynamically.

***

### <div align="center">Solving Step or Analysis</ins></div>
- Create a list for ticket IDs by taking data from the __SupportTicket__ sheet with the source:

````excel
        =SupportTickets!$A$2:$A$328
 ````
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/bbd30468-dbbb-4f3e-9bdd-c8e93388cfed" />

---

- Determine the lookup value → __Customer Name__ on the __SupportTickets Sheet__
- Set the reference data range in the __SupportTickets__ table
- Fill in the __Customer Name__ column with the INDEX + MATCH formula:

````excel
        =INDEX(Table1[Customer Name];MATCH(Sheet1!$C$3;Table1[Ticket ID];0))
 ````

<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/18b69f4c-3d31-4bc9-9d66-0edeff2f62a9" />

---

- Determine the lookup value → __Issue Type__ on the __SupportTickets Sheet__
- Set the reference data range in the __SupportTickets__ table
- Fill in the __Issue Type__ column with the INDEX + MATCH formula:

````excel
        =INDEX(Table1[Issue Type];MATCH(Sheet1!$C$3;Table1[Ticket ID];0))
 ````
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/e0845fc3-45f8-4736-aaa5-77471f905897" />

---

1️⃣
- Determine the lookup value → __Assigned Agent__ on the __SupportTickets Sheet__
- Set the reference data range in the __SupportTickets__ table
- Fill in the __Assigned Agent__ column with the INDEX + MATCH formula:

````excel
        =INDEX(Table1[Assigned Agent];MATCH(Sheet1!$C$3;Table1[Ticket ID];0))
 ````
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/39e9ad6d-329c-490e-bb51-9611e399d4d3" />

---

2️⃣
- Determine the lookup value → __Priority__ on the __SupportTickets Sheet__
- Set the reference data range in the __SupportTickets__ table
- Fill in the __Priority__ column with the INDEX + MATCH formula:

````excel
        =INDEX(Table1[Priority];MATCH(Sheet1!$C$3;Table1[Ticket ID];0))
 ````
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/c9ea2762-d290-4fe9-b2c3-a396e5a29dfc" />

---

3️⃣
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/acce5ba0-a4eb-4747-8cb3-d4d6c6a9b96c" />

---

<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/9118068c-d6d9-4515-8904-95248be8a42e" />

---

4️⃣
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/96fc9bd4-1e84-43ea-9117-c9f2de168f75" />

***

### <div align="center">Results Overview</ins></div>
