# 🛒 Walmart Sales Analysis Dashboard – Power BI Project

This repository contains my end-to-end **Walmart Sales Analysis Project** built entirely in **Power BI**. It simulates a real-world business analyst scenario using sales data to uncover insights, trends, and performance drivers across different time periods and regions.

---

## 📌 Project Objective

The goal of this project is to:
- Analyze Walmart sales performance across time, stores, and regions
- Track and compare KPIs like Total Sales, YTD Sales, and Growth
- Use advanced DAX and time intelligence functions
- Design professional dashboards with clean visuals
- Demonstrate practical skills expected from a Business/Data Analyst

## ❗ Business Problem

Walmart, a retail giant, operates hundreds of stores across various regions. However, decision-makers face challenges in quickly understanding:

- Which stores are underperforming or overachieving?
- How do holiday periods affect sales performance?
- What is the overall sales trend across months and years?
- How do different regions contribute to total revenue?

The business needs a **centralized dashboard** that allows management to:

- Track key performance indicators (KPIs)
- Compare current vs previous year sales
- Analyze store-wise, region-wise, and time-based performance
- Make data-driven decisions to optimize sales strategy

## 📊 Tools & Technologies Used

| Tool/Feature           | Purpose                                      |
|------------------------|----------------------------------------------|
| **Power BI Desktop**   | Main tool for data visualization & modeling |
| **Power Query Editor** | Data cleaning, transformation               |
| **DAX**                | Creating measures, KPIs, time intelligence  |
| **Data Modeling**      | Relationships, lookup tables                |

---

## 📁 Project Structure

| File/Folder                  | Description                                 |
|-----------------------------|---------------------------------------------|
| `Walmart_sales_analysis.csv`| Raw sales dataset                           |
| `Walmart_Dashboard.pbix`    | Full Power BI report file                   |
| `Screenshots/`              | Dashboard preview images                    |
| `README.md`                 | Project documentation (this file)          |

---

## 📈 Dashboard Features

✅ **Page 1: Executive Overview**
- **KPI Cards**: Total Sales, YTD Sales, Sales Growth
- **100% Stacked Bar Chart**: Regional sales share
- **Trend Chart**: Sales over time (Monthly or Weekly)
- **Slicers**: Year, Region, and Store filters

✅ **Page 2: Store & Performance Insights**
- **Store Ranking** using `RANKX()`
- **% of Total Sales** using `DIVIDE()` with `ALL()`
- **Time Comparison**: Current Year vs Last Year Sales
- **Holiday vs Non-Holiday Sales** (if available)

---

## 🧠 Key DAX Measures Used

```DAX
Total Sales = SUM('Walmart_sales_analysis'[Weekly_Sales_Amount])

Sales LY = 
CALCULATE(
    SUM('Walmart_sales_analysis'[Weekly_Sales_Amount]),
    SAMEPERIODLASTYEAR('Walmart_sales_analysis'[Invoice Date])
)

% of Total Sales = 
DIVIDE(
    SUM('Walmart_sales_analysis'[Weekly_Sales_Amount]),
    CALCULATE(
        SUM('Walmart_sales_analysis'[Weekly_Sales_Amount]),
        ALL('Walmart_sales_analysis')
    )
)



💼 What I Learned
Hands-on Power BI dashboard creation from scratch

Data modeling and relationship design

Time intelligence using functions like TOTALYTD(), SAMEPERIODLASTYEAR()

Formatting visuals, using bookmarks, slicers, and tooltips

Business storytelling using data

🚀 How to Use
Download or clone this repository

Open Walmart_Dashboard.pbix in Power BI Desktop

Review the pages and interact with the slicers

Modify and extend based on your learning goals

📸 Dashboard Preview
(https://github.com/Muhammadikramnawaz/Walmart-Sales-Performance-Dashboard/blob/main/walmart%20sales%20dashboard%20for%20github.png)

👋 About Me
I'm a Computer Science graduate currently learning Business Intelligence & Data Analytics. This project showcases my Power BI skills and is part of my journey to become a Business Analyst.

💬 Let's Connect
Feel free to fork, review, or contact me for feedback and collaboration.
I’m open to internship opportunities where I can apply and grow these skills!


### 📌 **Repository Name**  
`walmart-powerbi-dashboard`

### 📝 **Description**  
Power BI Sales Analysis Dashboard project for Walmart data. Uses DAX, Time Intelligence, and KPI cards to simulate real-world business analyst tasks.










