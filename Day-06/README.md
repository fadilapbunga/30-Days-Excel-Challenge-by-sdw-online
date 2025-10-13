# 6️⃣ Day 6: Conditional formatting – part 1

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

## Identification Database
To practice Conditional Formatting, there are 2 sheets to help highlight pattenrns and outliners. The sheets are 'Online Orders' and 'Sandwich Shop'.

- The 'Online Orders' column sheet consists of: Order ID, Customer, Order Value ($), Delivery Delay (days), Rating (out of 5).
<img width="397" height="511" alt="image" src="https://github.com/user-attachments/assets/06e67e51-f871-4dba-bbc1-2881dce5e1c3" />

- The 'Sandwich Shop' column sheet consists of: Month, Sandwich Sales, Juice Sales, Total Profit.
<img width="529" height="320" alt="image" src="https://github.com/user-attachments/assets/7325031b-750d-43bb-bbf9-691f29a75744" />


***

## Identification Issues
<img width="960" height="510" alt="image" src="https://github.com/user-attachments/assets/bcf8bdd3-a7bd-464e-9196-53591b0ed6c9" />

***

## Solving Step or Analysis
***Online Order Sheet**
- Highlight Order Values below $150 in red using Conditional Formatting 'Less Than'.
<img width="1033" height="700" alt="image" src="https://github.com/user-attachments/assets/a3cfcf9f-b59b-4544-b25a-2b7af3f30b9c" />

- Highlight Delivery Delays of 0 days in green using Conditional Formatting 'Equal To'.
<img width="1312" height="1021" alt="image" src="https://github.com/user-attachments/assets/389f7d78-9553-4df4-89dd-70c855dd7216" />

- Highlight Ratings below 3.5 in yellow using Conditional Formatting 'Less Than'
<img width="637" height="338" alt="image" src="https://github.com/user-attachments/assets/010c934a-17da-405b-ad6a-37119f45136c" />


***

**Sandwich Shop Sheet**
- Add Data Bar to Juice Sales located in C2:C11
- Add traffic light icons for Total Profit located in D2:D11
- Add a 3-color scale for Sandwich Sales located in B2:B11
<img width="1926" height="1022" alt="image" src="https://github.com/user-attachments/assets/3b0b47e7-1a2c-4ec8-b578-5c6937314ad5" />

***


## Results Overview
**Online Order Sheet**
- There are 61 whose Order Values are below than $150
- There are 22 whose doesn't have Delivery Delay
- There are 185 whose Ratings are below 3.5

**Sandwich Shop Sheet**
- Of the Sandwich Sales column, white is the most popular color and red is the least popular.
- Of the Juice Sales column, the least sales have short line data bar but for the most popular sales have long line data bar.
- Of Total Profit column, the black one have the least profit, the gray one have the middle profit, and the red one have the most profit.
