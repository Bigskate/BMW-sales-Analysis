🚗 BMW Sales Data Analysis — SQL + Power BI Dashboard

A complete end-to-end analytics project exploring BMW sales performance using SQL Server & Power BI.

📌 Project Overview

This project analyzes BMW car sales using a dataset containing model, year, region, mileage, price, transmission, fuel type, color, sales volume, and more.

The goal was to uncover insights into pricing patterns, mileage distribution, sales trends, model performance, and year-over-year growth.

I used:

SQL Server → Data cleaning, transformation & exploration

Power BI → Data modeling & visualization

VS Code → Organizing SQL scripts

GitHub → Documentation & portfolio presentation

🛠 Technologies Used
Tool	Purpose
SQL Server	Querying, cleaning, exploring the dataset
VS Code	Writing & saving SQL scripts
Power BI	Creating interactive dashboards
GitHub	Hosting the project & documentation
🧹 1. Data Cleaning & Preparation (SQL)
🔹 Cleaning Steps Performed

Removed rows with missing values

Converted year to numeric

Ensured price & mileage columns were numeric

Standardized fuel type and transmission values

Checked and removed duplicates

Prepared the dataset for Power BI modeling

📎 Sample SQL (Cleaning)
-- Remove rows with missing price or mileage
SELECT *
FROM BMW Sales Table
WHERE price IS NOT NULL
  AND mileage IS NOT NULL;


More SQL scripts are included in the /SQL folder.

2. SQL Analysis
Summary Metrics
SELECT 
    SUM(SalesVolume) AS TotalSales,
    SUM(price) AS TotalRevenue,
    AVG(price) AS AvgPrice,
    AVG(mileage) AS AvgMileage
FROM BMW Sales Table;

Model Performance
SELECT model,
       COUNT(*) AS TotalSales,
       AVG(price) AS AvgPrice
FROM BMW Sales Table
GROUP BY model
ORDER BY TotalSales DESC;

Year-over-Year Trends
SELECT 
    year,
    SUM(price) AS YearRevenue
FROM BMW Sales Table
GROUP BY year
ORDER BY year;

📈 3. Power BI Dashboard

The dashboard contains three pages, each highlighting a different part of the analysis.

📌 Page 1 – Sales Overview

Total Sales

Total Revenue

Average Price

Average Mileage

Sales by Model

Sales by Region

YoY Growth KPI

Fuel Type distribution

📌 Page 2 – Pricing & Mileage Insights

Top Selling Product

Top Sales by Region

Top Sales by Color

Top Sales by Fuel Type

Revenue by Model 

Revenue by Region

Revenue by Year

🔍 4. Key Insights Discovered

Low-mileage vehicles generally command higher prices.

Certain BMW models consistently generate the highest total sales.

Regional analysis shows strong variations in demand and pricing.

YoY growth reveals strong performance in specific years.

✨ Conclusion

This project strengthened my skills in:

Writing efficient SQL queries

Data cleaning & transformation

Building interactive Power BI dashboards

Interpreting and communicating insights

I will continue building more projects and sharing my learning journey.
