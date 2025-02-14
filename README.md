# chocolates-Sales-Performance-Dashboard-Power-BI
This repository contains an interactive Sales Performance Dashboard built in Power BI. It provides deep insights into sales trends, revenue analysis, and key performance indicators using dynamic visualizations and DAX formulas.

## Overview
This repository contains a **Sales Performance Dashboard** built using Power BI. The dashboard offers insights into sales trends, revenue, top-performing products, and regional performance. It leverages **DAX (Data Analysis Expressions)** formulas for calculations and various Power BI visualizations.

## Features
- **Comprehensive Sales Analysis**
- **Dynamic and Interactive Visuals**
- **Filtering and Drill-through Analysis**
- **Calculated Metrics using DAX**
- **Automated Data Refresh**

## DAX Formulas Used
The following **DAX formulas** were used in the report:

### Aggregation & Totals:
- `SUM(Sales[Amount])` - Calculates total sales revenue.
- `SUMX(Sales, Sales[Quantity] * Sales[Price])` - Computes total revenue dynamically.

### Conditional Calculations:
- `IF(TOTALYTD(SUM(Sales[Amount]), Dates[Date]) > 50000, "High", "Low")` - Categorizes sales performance.

### Time Intelligence:
- `TOTALYTD(SUM(Sales[Amount]), Dates[Date])` - Calculates Year-to-Date (YTD) sales.
- `PREVIOUSMONTH(SUM(Sales[Amount]))` - Fetches previous month's sales data.
- `DATEADD(Sales[Date], -1, YEAR)` - Returns sales for the same period last year.

### Ranking & Performance Metrics:
- `RANKX(ALL(Sales[Product]), SUM(Sales[Amount]), , DESC, DENSE)` - Ranks top-selling products.
- `DIVIDE(SUM(Sales[Profit]), SUM(Sales[Revenue]), 0)` - Calculates profit margin.

## Visualizations Used
The Power BI dashboard includes the following **visualization charts**:

1. **Bar Chart** - Displays top-selling products by revenue.
2. **Line Chart** - Shows monthly sales trends.
3. **Pie Chart** - Represents revenue distribution by category.
4. **Table Visual** - Lists detailed sales data with KPIs.
5. **Map Visual** - Highlights sales performance by region.
6. **KPI Cards** - Show total revenue, profit margin, and total orders.
7. **Slicer Filters** - Enable interactive filtering by date, category, and region.

## How to Use
1. Download the Power BI file: **project file.pbix**
2. Open it using **Power BI Desktop (Recommended: Latest Version).**
3. Interact with the visuals, filters, and slicers to analyze sales trends.
4. Connect to a data source if required and refresh the data.


## Contributions
Contributions are welcome! If you have suggestions for improvements, feel free to open an issue or submit a pull request.

## License
This project is open-source and available under the MIT License.

