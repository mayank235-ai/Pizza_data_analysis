🍕📊 Pizza Sales Analytics – Insights from Data to Dashboard

This project dives into pizza sales performance using a combination of PostgreSQL for SQL-based analysis and Excel for dashboard visualization.
The goal is to understand customer buying habits, identify top-performing pizzas, and draw meaningful insights that can guide business strategies.


📂 Dataset Overview

The dataset contains detailed information on pizza orders — including order IDs, pizza names, quantities, prices, order dates, and times.
You can find the dataset in this repository once uploaded.



🧰 Tools & Technologies

PostgreSQL – Database management and data analysis

Microsoft Excel – Visualization and dashboard creation

Power Query – Data import and transformation

Pivot Tables & Charts – Summary metrics and KPIs



---

🔄 Project Workflow

🪜 Step 1: Data Import

The raw dataset was loaded into PostgreSQL using its import tool.
A pizza_sales table was created with the following key columns:

order_id, pizza_id, pizza_name_id, quantity, order_date, order_time, unit_price, total_price


🧹 Step 2: Data Cleaning

Removed blank rows and invalid entries

Corrected date and time formats

Standardized category and size values for consistency


💻 Step 3: SQL Analysis

Once the data was cleaned, SQL queries were used to extract important metrics such as:

Total Revenue

SELECT SUM(total_price) AS total_revenue FROM pizza_sales;

Average Order Value

SELECT SUM(total_price) / COUNT(DISTINCT order_id) AS avg_order_value FROM pizza_sales;

Most Popular Pizzas

SELECT pizza_name_id, SUM(quantity) AS total_sold
FROM pizza_sales
GROUP BY pizza_name_id
ORDER BY total_sold DESC
LIMIT 5;

In addition to these, time-based and category-wise breakdowns were also explored to identify sales trends.

📊 Step 4: Excel Dashboard

The query outputs were exported to Excel to build an interactive dashboard using:

Pivot Tables for data summarization

Charts (line, bar, donut) for trend visualization

Slicers for filtering by category, size, and date



---

📈 Major Insights

💰 Sales Highlights

Total revenue: $817,860

Peak sales on Fridays and Saturdays

High order volume during lunch (12–1 PM) and evening (5–8 PM)


🍕 Product Insights

Most ordered size: Large

Top-selling pizza: Classic Deluxe Pizza

Top revenue category: Classic pizzas


⚠️ Low Performers

Least ordered pizzas: Brie Carre and Mediterranean



---

🧾 Dashboard Sneak Peek

An Excel dashboard was designed to visually track KPIs such as revenue, order trends, and category performance.
https://github.com/mayank235-ai/Pizza_sales_analysis/blob/main/pizza_dashboad.png



📁 Repository Structure

Pizza_Sales_Analysis 

├── pizza_sales.csv

├── queries.sql

├── pizza_sales_dashboard.png

├── README.md



