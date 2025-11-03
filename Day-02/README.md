# 2️⃣ Day 2: Formatting for analysis

## 📝 Table of Contents
  - [Identification Database](#identification-database)
  - [Identification Issues](#identification-issues)
  - [Solving Step / Analysis](#solving-step-or-analysis)
  - [Results Overview](#results-overview)

***

### <div align="center">Identification Database</ins></div>
The data contains freelance project data. That contains the name of client and project with hourly rates. 
- __'Fee'__ column shows the total number of fee in a few hours.
- __'Start Date'__ column shows since when the project started.
- __'Completed'__ column shows whether the project is complete or not.
  
<img width="960" height="509" alt="Image" src="https://github.com/user-attachments/assets/94b0e9cc-2e2f-4026-9d41-be2f2f73a9a3" />

***

### <div align="center">Identification Issues</ins></div>
- Use the PROPER function to capitalize project names.
- Format the 'Fee' and 'Fee per Hour' columns as currency (US Dollars).
- Format the 'Start Date' column to show dates like: 15-Jan-2024.
- Standardize the 'Completed' column to only show 'Yes' or 'No'.
- Auto-fit all columns so values are fully visible.
- Highlight rows where 'Fee per Hour' is below $75 using conditional formatting.
- Make the header row bold and add a bottom border.

***

### <div align="center">Solving Step or Analysis</ins></div>
__1.__
- Use __=Proper__ at another column to capitalize project name column like at column I.
<img width="1920" height="1018" alt="Image" src="https://github.com/user-attachments/assets/d6cc4373-45f7-44d6-ae6d-37d5eb1cc74d" />

---

- And then Copy the values into the initial column. The result is that every project name list has its first letter capitalized.
<img width="960" height="509" alt="Image" src="https://github.com/user-attachments/assets/e7b49268-7fdf-412f-9d3a-a0b382830efa" />

***

__2.__
- To change 'Fee' and 'Fee per Hour' columns as __currency (US Dollars)__, at Home tab, change the __Accounting__ format into __US Dollar__ like the picture below. 
<img width="1922" height="816" alt="Image" src="https://github.com/user-attachments/assets/8c78c19b-4025-42af-bdbd-3e3de2a45c2a" />
<img width="960" height="509" alt="Image" src="https://github.com/user-attachments/assets/828728e4-9b78-403c-b663-acc9ace13f17" />

***

__3.__
- Change the format of Start Date type with __'dd-mmmm-yy'__ to get the show dates like the format: __15-Jan-2024.__
<img width="1942" height="1022" alt="Image" src="https://github.com/user-attachments/assets/46974d86-ffda-4bd5-b3d6-0de9cf16cdc2" />
<img width="960" height="509" alt="Image" src="https://github.com/user-attachments/assets/1b1ed1f3-4642-4f9c-be7b-7db6acada630" />


__4.__
- Before standardize the 'Completed' column to only show 'Yes' or 'No', change the words of 'Yes' and 'No' by using __Proper__ formula so that only the first letter is capitalized, making the writing look neater. And then Copy the values into the initial column.
<img width="1920" height="1018" alt="Image" src="https://github.com/user-attachments/assets/fbe15d21-0d3e-40a3-ab25-df53e77bbeda" />

---

- After that, use the __Filter__ feature to standardize the ‘Completed’ column so that it only displays ‘Yes’ or ‘No’. We can change it if we want to display one or both.
<img width="1922" height="1024" alt="Image" src="https://github.com/user-attachments/assets/a5e51619-efb4-4a27-b6f5-367017dec9e6" />
<img width="1924" height="1020" alt="Image" src="https://github.com/user-attachments/assets/91fc0229-eb47-4e87-9a76-ce5ad6521d20" />

***

__5.__
- Check again one more time, make sure to __auto-fit__ all columns values so that the value is clearly legible.
<img width="960" height="509" alt="Image" src="https://github.com/user-attachments/assets/30ed3806-7943-4d27-b382-f8ea12f878b8" />

***

__6.__
- Using __Conditional Formatting__ to higlight the Fee per Hour that less than $75, and color with red. <aking it easier to see at a glance which ones have a higher value or not.
<img width="1920" height="1024" alt="Image" src="https://github.com/user-attachments/assets/4a812341-bd61-4c6d-802c-f8a9d2a348d6" />
<img width="960" height="509" alt="Image" src="https://github.com/user-attachments/assets/faa37763-f79f-4ab8-a7e6-134c30514d5c" />

***

__7.__
- Adding __Bottom Border__ at Home tab
<img width="1920" height="1018" alt="Image" src="https://github.com/user-attachments/assets/2466b628-c6e5-48d6-bc0c-97a0bf15e097" />
<img width="960" height="510" alt="Image" src="https://github.com/user-attachments/assets/f7c98f88-e463-48ef-ad35-6ac6cabb4e19" />


***


### <div align="center">Results Overview</ins></div>
- The project data has been tidied up to make it clearer, more uniform, and ready for analysis. Project names have been capitalized correctly using the __PROPER__ function, while the Fee and Fee per Hour columns have been __formatted into US Dollars__. Project start dates are displayed in an easy-to-read format, such as 15-Jan-2024, and the Completed column now only displays Yes or No options to ensure data consistency.
- All columns have also been set to __AutoFit__ so that the table contents are fully visible without being cut off. For easy identification, rows with an Hourly Fee below $75 are automatically highlighted using __conditional formatting__. The table title row is bolded and underlined for a neater and more professional look.
<div align="center"><img width="960" height="509" alt="Image" src="https://github.com/user-attachments/assets/ae07fe17-6f9c-4f36-8943-3999d55f8a93" /></ins></div>
