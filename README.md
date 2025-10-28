🍕📊 Pizza Sales Analytics — Turning Data into Delicious Insights

Welcome to my Pizza Sales Analytics Project, where I combined PostgreSQL and Microsoft Excel to transform raw pizza order data into a story of sales trends, customer behavior, and business insights.

The project demonstrates end-to-end data analysis skills — from data cleaning and SQL exploration to interactive dashboard creation — providing actionable insights that a pizza business can actually use to boost revenue and efficiency.

🎯 Project Objective

To analyze historical pizza sales data and answer key business questions such as:

Which pizzas and categories generate the most revenue?

When do sales peak during the day or week?

What size and category combinations perform best?

Which products are underperforming and need marketing attention?

By the end, the analysis highlights clear sales drivers and improvement opportunities through both SQL queries and interactive Excel dashboards.

📦 Dataset Description

The dataset represents one year of transactional data from a fictional pizza store.

Column Name	Description
order_id	Unique identifier for each order
pizza_id	Unique ID for each pizza sold
pizza_name_id	Coded pizza name
quantity	Number of pizzas ordered
order_date	Date of the order
order_time	Time of the order
unit_price	Price per pizza
total_price	Total price for that line item
pizza_category	Category of pizza (Classic, Veggie, etc.)
pizza_size	Size of pizza (S, M, L, XL, etc.)


🧰 Tools & Technologies Tool	Purpose

🐘 PostgreSQL	Data storage, SQL querying, and analysis
📊 Microsoft Excel	Dashboard design and data visualization
⚙️ Power Query	Data import and transformation
📈 Pivot Tables & Charts	KPI visualization and trend exploration

🔍 Project Workflow
1️⃣ Data Import and Setup

Imported the raw CSV into PostgreSQL.

Created the pizza_sales table with appropriate data types.

Validated successful data load using SELECT COUNT(*) FROM pizza_sales;.

2️⃣ Data Cleaning

Removed rows with null or invalid entries.

Standardized pizza categories and sizes.

Converted date and time columns to proper formats for time-based analysis.

3️⃣ SQL-Based Analysis

Key analytical queries performed in PostgreSQL include:

Total Revenue

SELECT ROUND(SUM(total_price), 2) AS total_revenue FROM pizza_sales;


Peak Order Hours

SELECT EXTRACT(HOUR FROM order_time) AS hour, COUNT(order_id) AS order_count
FROM pizza_sales
GROUP BY hour
ORDER BY order_count DESC;


Top-Selling Pizzas

SELECT pizza_name_id, SUM(quantity) AS total_sold
FROM pizza_sales
GROUP BY pizza_name_id
ORDER BY total_sold DESC
LIMIT 5;


These queries provided the foundation for visual KPIs in Excel.

📊 Dashboard Development

After analysis, results were exported to Excel to build a dynamic, interactive dashboard that visualizes:

💰 Total Revenue, Average Order Value, and Total Orders

⏰ Sales Trends by Hour and Day of Week

🍕 Top & Bottom Performing Pizzas

📏 Sales Distribution by Pizza Size & Category

Interactive Slicers were added to filter by pizza category and size, allowing business managers to explore data from multiple angles.

💡 Key Insights
Area	Insight
Revenue	Total revenue generated was $817,860, with consistent growth toward weekends.
Time Trends	Sales peak during 12 PM – 1 PM and 5 PM – 8 PM, aligning with lunch and dinner rush hours.
Product Preferences	The Large size and Classic category dominate sales.
Top Performer	The Classic Deluxe Pizza had the highest number of sales and revenue.
Low Performer	Brie Carre and Mediterranean Pizza saw minimal demand — potential discontinuation candidates.

These insights provide a strong foundation for marketing campaigns, inventory planning, and menu optimization.

🧾 Dashboard Snapshot

📈 Download and explore the interactive Excel dashboard:
Pizza Sales Dashboard (Excel)
 https://github.com/mayank235-ai/Pizza_data_analysis/blob/main/pizza_dashboad.png
 
📁 Repository Structure
Pizza_Sales_Analytics/
│
├── data/
│   └── pizza_sales.csv
│
├── sql/
│   └── analysis_queries.sql
│
├── dashboard/
│   └── pizza_sales_dashboard.xlsx
│
└── README.md

