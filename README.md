# Mobile_Sales_Power-BI
# 📊 Power BI Mobile_Sales Dashboard Project

## 📌 Project Summary
This project is an  end-to-end Power BI Sales Dashboard built to analyze sales performance, customer behavior, and product trends.  
It demonstrates skills in data cleaning, data modeling, DAX, time intelligence, and dashboard design.

---

## 🧹 Step 1: Data Cleaning
- Cleaned raw data using **Power Query**
- Removed errors and handled missing values
- Standardized column names and formats
- Ensured data accuracy for reporting

---

## 📅 Step 2: Custom Calendar Table
A custom calendar table was created to support:
- Day-wise sales analysis
- Cumulative sales calculation
- Time intelligence functions (MTD, QTD, YTD)

### Why a Calendar Table?
- Required for time-based calculations
- Enables month-wise and day-wise trends
- Improves accuracy of DAX time intelligence

---

## 🛠 Step 3: Calendar Creation (Power Query)
**Steps followed:**
1. Power Query Editor → Home → New Source → Blank Query  
2. Open Advanced Editor / fx  
3. Used the formula:

= List.Dates(#date(2021,1,1), 1461, #duration(1,0,0,0))

- Calendar created for **4 years starting from 2021**
- Converted list into table format
- Renamed columns appropriately

---

## 📦 Data Modeling
### Fact Table
- Stores numerical and transactional data  
  (Sales, Quantity, Transactions)

### Dimension Tables
- Stores descriptive data  
  (Calendar, Product, Brand, City)

**Benefits:**
- Better model structure
- Improved performance
- Accurate reporting

---

## 🧮 DAX Measures & Calculated Columns
### Measures Created:
- Total Sales  
- Total Quantity  
- Average Price  
- Total Transactions  

### Calculated Columns:
- **Total Sales Column:** Price per Unit × Units Sold
- **Rating Status:** Created using `IF` function
- **Day Name Column:**
DayName = FORMAT('Calendar'[Date], "dddd")

---

## 🎨 Dashboard Design
- Consistent color theme  
  **Primary Color:** `#3D83C9`
- Custom background using a mobile phone image
- Month slicer created using the custom calendar
- Clean, user-friendly layout

---

## 📊 Visualizations Included
- KPI Cards – Total Sales, Quantity, Transactions, Average Price
- Map – Total Sales by City
- Line Chart – Monthly Quantity Trend
- Funnel Chart – Rating Status
- Pie Chart – Transactions by Payment Mode
- Bar Chart – Top 3 Mobile Models by Sales
- Area Chart – Total Sales by Day Name
- Table – Top 5 Brands with Transactions and Total Sales

---

## ⏱ Time Intelligence (MTD, QTD, YTD)
The dashboard was duplicated to create:
- MTD (Month-to-Date)
- QTD (Quarter-to-Date)
- YTD (Year-to-Date)

### MTD DAX Formula:
MTD = TOTALMTD([Total_Sales], 'Custom Calendar'[Date])

- MTD values visualized using a line chart
- Same logic applied for QTD and YTD

---

## ✅ Final Outcome
- Built an interactive and dynamic Power BI dashboard
- Enabled advanced time-based analysis
- Delivered insights into sales performance and product trends
- Dashboard suitable for both business users and management

---

## 🛠 Tools Used
- Power BI
- Power Query
- DAX
- Data Modeling 
