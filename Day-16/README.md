# 1️⃣6️⃣ Day 16: VLOOKUP + HLOOKUP

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

### <div align="center">Identification Database</ins></div>
There are two datasets originating from Warehouse Operations for a retail company. 

✅ __Dataset 1 (Sheet: ProductShipments)__:
- List of product shipments across various warehouses
- Fields: __Product ID, Product Name, Category, Warehouse, and Region.__

✅ __Dataset 2 (Sheet: ShippingRules)__:
- Shipping rules by Region
- Columns: East, West, North, South
- Rules: __Max Weight, Delivery Time, and Shipping Cost.__

***

### <div align="center">Identification Issues</ins></div>
✅ __Tasks:__
1. Use VLOOKUP to find which warehouse a product is stored in using its Product ID.
2. Use VLOOKUP to get the product's Region from the same table.
3. Use HLOOKUP to get the Max Weight allowed for that Region.
4. Use HLOOKUP to get the Delivery Time and Shipping Cost for that Region.
5. BONUS: Create a dropdown menu to select a Product ID and auto-fill the other fields.

***

### <div align="center">Solving Step or Analysis</ins></div>

1️⃣
- Create a new sheet containing the data to be processed for the VLOOKUP + HLOOKUP exercise.
- Create a data table as shown below, where the __Product ID__ row becomes a list by:
- Opening the __Data menu → Data Validation__.
- Selecting __“List”__.
- Entering the following formula:

````excel
        =ProductShipments!$A$2:$E$333
 ````
<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/a17be83c-3f4d-4780-b96f-4c411b4a1771" />

---

- To find which warehouse a product is stored in using its Product ID, use the __=VLOOKUP__ formula as shown below, where the __lookup_value is the Product ID row itself, the table_array is in the ProductShipments sheet, and the col_index_num is 4__ because the warehouse is in column 4.
- When selecting another product ID, the warehouse data will follow.

````excel
        =VLOOKUP($C$6;Table1;4;FALSE)
 ````
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/9c6ad5ef-8cd9-4ac1-b103-542d12a2e9f6" />

---

2️⃣
- To find the product's Region from the same table, use the __=VLOOKUP__ formula as shown below, where the __lookup_value is the Product ID row itself, the table_array is in the ProductShipments sheet, and the col_index_num is 5__ because the region is in column 5.

````excel
        =VLOOKUP($C$6;Table1;5;FALSE)
 ````
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/487798ac-5ef1-4751-98f4-55527aac6966" />

- Next, to fill in the __Product Name__ and __Category__ rows, use the same formula as above, but the only difference is in __col_index_num__. For Product Name, it is in column number __2__, and for Category, it is in column number __3__.
  
---

3️⃣
- To find __Max Weight (Kg)__ allowed for that Region, use the __=HLOOKUP__ formula as shown below, where the __lookup_value is the Region row itself, the table_array is in the ShippingRules sheet, and the col_index_num is 2__ because the __Max Weight (Kg)__ is in row 2.

````excel
        =HLOOKUP($C$4;ShippingRules!$A$1:$E$4;2;FALSE)
 ````
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/803c9fa8-a4ec-4e37-90c6-c23766e466f1" />

---

4️⃣
- To find __Delivery Time (Days)__ for that Region, use the __=HLOOKUP__ formula as shown below, where the __lookup_value is the Region row itself, the table_array is in the ShippingRules sheet, and the col_index_num is 3__ because __Delivery Time (Days)__ is in row 3.

````excel
        =HLOOKUP($C$4;ShippingRules!$A$1:$E$4;3;FALSE)
 ````
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/eec80856-4614-4305-aa1f-f04b88d62566" />

---

- To find __Shipping Cost($)__ for that Region, use the __=HLOOKUP__ formula as shown below, where the __lookup_value is the Region row itself, the table_array is in the ShippingRules sheet, and the col_index_num is 4__ because __Shipping Cost ($)__ is in row 4.

````excel
        =HLOOKUP($C$4;ShippingRules!$A$1:$E$4;4;FALSE)
 ````

<img width="1920" height="1018" alt="image" src="https://github.com/user-attachments/assets/08920b25-46eb-4aef-b5dc-751d011be279" />

***

### <div align="center">Results Overview</ins></div>
- Today I learned two important functions in Excel: VLOOKUP and HLOOKUP.
Both are like “automatic search tools,” only they differ in direction—one searches downwards, the other searches sideways.
With this exercise, I now understand better how Excel can retrieve data with just one keyword, without having to search manually.
This exercise has made me more comfortable working with large tables and faster at finding important information.
