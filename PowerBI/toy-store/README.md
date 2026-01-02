# Basic Toy Store Power BI Report

## 🧸 Project Overview
This Power BI report analyzes sales performance, inventory, and profitability for a basic toy store model. It focuses on **data cleaning**, **KPIs**, and **DAX calculations** to provide actionable insights for store managers and decision-makers.

---

## ✅ Objectives
- Clean and standardize raw sales and inventory data.
- Build KPIs for revenue, profit, and stock levels.
- Visualize performance by product category, store location, and time.
- Enable drill-through for product-level and regional analysis.

---

## 🧹 Data Cleaning Steps (Power Query)
- **Removed duplicates** from sales and product tables.
- **Standardized column names** (e.g., `OrderDate`, `ProductCategory`, `Revenue`).
- **Handled missing values**:
  - Filled nulls in `ProductCategory` with `"Miscellaneous"`.
  - Replaced blank revenue values with `0`.
- **Converted data types**:
  - Dates → `Date`
  - Revenue & Cost → `Decimal`
- **Created calculated columns**:
  - `TotalCost` = Unit Cost × Quantity
  - `Profit` = Revenue − TotalCost

---

## 📏 Core DAX Measures
Representative measures used in the report:

```DAX
-- Total Revenue
Total Revenue := SUM('Sales'[Revenue])

-- Total Cost
Total Cost := SUM('Sales'[TotalCost])

-- Total Profit
Total Profit := [Total Revenue] - [Total Cost]

-- Profit Margin %
Profit Margin % := DIVIDE([Total Profit], [Total Revenue])

-- Total Orders
Total Orders := COUNTROWS('Sales')

-- Average Order Value
Average Order Value := DIVIDE([Total Revenue], [Total Orders])

-- Inventory Stock
Current Stock := SUM('Inventory'[StockQuantity])
```

---

## 📊 Report Pages
1. **Executive Overview** – KPIs for revenue, profit, margin, and orders.
2. **Category Performance** – Revenue and profit by toy category.
3. **Inventory Analysis** – Stock levels and reorder alerts.
4. **Regional Insights** – Store-level performance and trends.

---

## 🖼 Screenshots
*(Add screenshots of your dashboards here using Markdown syntax)*
Example:
```markdown
![Overview Dashboard](images/overview.png)
![Inventory Analysis](images/inventory.png)
```

---

## 🔄 Refresh & Setup
1. Open `BasicToyStore.pbix` in Power BI Desktop.
2. Update data source paths in **Transform Data**.
3. Click **Refresh** to load cleaned data and apply DAX measures.

---

## 📂 Recommended Folder Structure
```
BasicToyStore/
├── BasicToyStore.pbix
├── README.md
└── images/
    ├── overview.png
    ├── category.png
    ├── inventory.png
    └── regional.png
```

---

## 🚀 Future Enhancements
- Add **time intelligence** (YTD, QoQ growth).
- Implement **RLS** for store managers.
- Include **forecasting** for seasonal demand.

---

## 📄 License & Attribution
This report uses a sample toy store dataset for demonstration purposes.
