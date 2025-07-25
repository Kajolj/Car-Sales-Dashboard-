# Car-Sales-Dashboard-
Car Sales Dashboard - Power BI Project
# Car Sales Dashboard – Power BI End‑to‑End Project

A comprehensive car sales analysis dashboard built with Power BI, following the “Car Sales Advanced DAX” tutorial (2024).

## Overview
This dashboard provides a robust analysis of car dealership performance, with dynamic KPIs, time-series insights, and model-level trends. Designed to help stakeholders identify top-selling vehicles, regions, and pricing patterns using advanced DAX logic and interactive visuals.

## Key Features
- **Time Intelligence Metrics**: Year‑to‑Date (YTD), Month‑to‑Date (MTD), and Year‑over‑Year growth for sales revenue and units.
- **Advanced Visualizations**:
  - Line charts showing weekly YTD sales trends with highlighted peak points.
  - Pie/Donut charts for body style, color, engine, and transmission-level analysis.
  - Map visuals for geographic sales distribution.
  - Table and matrix layouts for detailed breakdowns.
- **Interactivity**: Filters (slicers) on dealer region, body style, transmission, engine type.
- **Navigation**: Multi-page layout for drill-down and summary perspectives.

## Core DAX Measures (examples)
- `YTD Total Sales = TOTALYTD(SUM(car_data[Price]), 'Date'[Date])`
- `Previous Year YTD = CALCULATE(SUM(car_data[Price]), SAMEPERIODLASTYEAR('Date'[Date]))`
- `YOY Growth = DIVIDE([YTD Total Sales] - [Previous Year YTD], [Previous Year YTD])`
- `YTD Units Sold = TOTALYTD(COUNTROWS(car_data), 'Date'[Date])`
- `Max Weekly Point = IF(MAXX(ALLSELECTED('Date'[Week]), [Total Sales]) = [Total Sales], [Total Sales], BLANK())`

## Data Model
- Star schema with fact table (`car_data`) and `Date` dimension.
- Monthly, weekly hierarchies to support time-based analysis.

## Usage
1. Clone or download this repository.
2. Open `Car_Sales_Dashboard.pbix` in Power BI Desktop.
3. Use slicers to filter by region, body style, engine, etc.
4. Navigate through report pages to explore overall metrics and detailed trends.

##  Skills Demonstrated
- Power Query for data cleaning and transformation
- Data modeling and relationship design
- Advanced DAX functions for time intelligence and dynamic KPIs
- Interactive data storytelling through visuals and slicers
- Performance optimization and design best practices

## 📌 Credits
Built by Kajol jadhav, based on the tutorial *Power BI Project From Start to End Part 1 | Car Sales | Advanced DAX Functions* (2024) (https://youtu.be/XnPo5Ft7RzQ?feature=shared)

