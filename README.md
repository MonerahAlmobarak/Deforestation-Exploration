# Deforestation Exploration

This project analyzes global forestation trends between 1990 and 2016 to support ForestQuery, a non-profit organization committed to raising awareness and reducing deforestation worldwide.

## 🌍 Project Introduction

As a data analyst at ForestQuery, your goal is to provide actionable insights into:

- Which countries and regions have experienced significant forest loss.
- Which countries and regions maintain the highest forest coverage, both in total area and as a percentage of land.

These insights are intended to inform executive decision-making regarding initiatives, communications, and resource allocation.

The analysis combines multiple datasets to explore trends and regional differences, helping the ForestQuery leadership team prioritize efforts for maximum environmental impact.

## 📚 Lesson Context

This project was created as part of a data analytics learning path. It involves relational database skills, data transformation, and analytical thinking using SQL.

## 📥 Data Sources

Three tables were provided for analysis:

- **forest_area**: Forest size per country and year (in sq km).
- **land_area**: Total land area per country and year (in sq mi).
- **regions**: Country-to-region mappings.

The data spans the years **1990 to 2016**.

## 🧩 Project Steps

1. **Join Tables**  
   Create a SQL **View** named `forestation` that joins:
   - `forest_area` and `land_area` on `country_code` and `year`
   - `regions` on `country_code`

2. **Include Columns**  
   The view should contain:
   - All columns from the original tables
   - A **new column** calculating forest area as a **percentage of land area**

3. **Unit Conversion**  
   Since:
   - `forest_area` is in square kilometers
   - `land_area` is in square miles  
   
   You must convert land area to square kilometers before calculating the forest percentage:
forest\_percent = forest\_area\_sqkm / (land\_area\_sqmi \* 2.59)

4. **Output Preparation**  
Use the `forestation` view to generate insights and write a summary report for the executive team with key findings across countries and regions.

## 🎯 Deliverables

- A SQL View called `forestation`
- A summary report highlighting:
- Top countries and regions by forest area
- Areas with significant forest loss
- Forest area percentages across time

## 👤 Author

**Monerah Almobarak**  
