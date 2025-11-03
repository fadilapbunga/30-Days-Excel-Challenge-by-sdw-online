# 6️⃣ Day 6: Conditional formatting – part 1

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

### <div align="center">Identification Database</ins></div>
To practice Conditional Formatting, there are 2 sheets to help highlight pattenrns and outliners. The sheets are __'Online Orders'__ and __'Sandwich Shop'.__

- The __'Online Orders'__ column sheet consists of: __Order ID, Customer, Order Value ($), Delivery Delay (days), Rating (out of 5).__
<div align="center"><img width="397" height="511" alt="image" src="https://github.com/user-attachments/assets/06e67e51-f871-4dba-bbc1-2881dce5e1c3" /></ins></div>

- The __'Sandwich Shop'__ column sheet consists of:__Month, Sandwich Sales, Juice Sales, Total Profit.__
<div align="center"><img width="529" height="320" alt="image" src="https://github.com/user-attachments/assets/7325031b-750d-43bb-bbf9-691f29a75744" /></ins></div>


***

### <div align="center">Identification Issues</ins></div>
<img width="960" height="510" alt="image" src="https://github.com/user-attachments/assets/bcf8bdd3-a7bd-464e-9196-53591b0ed6c9" />

***

### <div align="center">Solving Step or Analysis</ins></div>
__1. Online Order Sheet__
- Highlight Order Values below $150 in red using Conditional Formatting __'Less Than'.__
<img width="1033" height="700" alt="image" src="https://github.com/user-attachments/assets/a3cfcf9f-b59b-4544-b25a-2b7af3f30b9c" />

---

- Highlight Delivery Delays of 0 days in green using Conditional Formatting __'Equal To'.__
<img width="1312" height="1021" alt="image" src="https://github.com/user-attachments/assets/389f7d78-9553-4df4-89dd-70c855dd7216" />

---

- Highlight Ratings below 3.5 in yellow using Conditional Formatting __'Less Than'.__
<div align="center"><img width="637" height="338" alt="image" src="https://github.com/user-attachments/assets/010c934a-17da-405b-ad6a-37119f45136c" /></ins></div>


***

__2. Sandwich Shop Sheet__
- Add __Data Bar__ to Juice Sales located in C2:C11
- Add __Traffic Light Icons__ for Total Profit located in D2:D11
- Add __A 3-Color Scale__ for Sandwich Sales located in B2:B11
<img width="1926" height="1022" alt="image" src="https://github.com/user-attachments/assets/3b0b47e7-1a2c-4ec8-b578-5c6937314ad5" />

***


### <div align="center">Results Overview</ins></div>
__1. Online Order Sheet__
- Using Conditional Formatting __'Less Than'.__ There are 61 whose Order Values are below than $150 marked in red.
- Using Conditional Formatting __'Equal To'.__ There are 22 whose doesn't have Delivery Delay marked in green.
- Using Conditional Formatting __'Less Than'.__ There are 185 whose Ratings are below 3.5 marked in yellow.

__2. Sandwich Shop Sheet__
- Of the Sandwich Sales column, the __Data Bar__ indicates that white is the most popular color and red is the least popular.
- Of the Juice Sales column, the __Traffic Light Icons__ indicates that the least sales have short line data bar but for the most popular sales have long line data bar.
- Of Total Profit column, __A 3-Color Scale__ indicates that the black one have the least profit, the gray one have the middle profit, and the red one have the most profit.
