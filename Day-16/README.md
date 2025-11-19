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

- To find which warehouse a product is stored in using its Product ID, use the VLOOKUP formula as shown below, where the __lookup_value is the Product ID row itself, the table_array is in the ProductShipments sheet, and the col_index_num is 4__ because the warehouse is in column 4.
- When selecting another product ID, the warehouse data will follow.

````excel
        =VLOOKUP($C$6;Table1;4;FALSE)
 ````
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/9c6ad5ef-8cd9-4ac1-b103-542d12a2e9f6" />




***

### <div align="center">Results Overview</ins></div>
