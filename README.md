# 📊 Sales Insights Dashboard - Power BI Project
🔗 **Overview**
This project visualizes sales performance data using Power BI. It connects to a MySQL database and an Excel file for comprehensive analysis. All data is cleaned, modeled, and visualized using Power BI's powerful features.

🧱 **Tech Stack**
Database: MySQL

External File: Excel (transactions.xlsx)

BI Tool: Power BI Desktop

ETL Tool: Power Query (in Power BI)

✅ ** Steps to Run the Project**

1. 🛠️ **Import SQL Dump into MySQL Workbench**
Open MySQL Workbench

Create a new schema/database (e.g., sales_db)

Open the sales_dump.sql file

Run the SQL script to create all tables

📌 Important: Ensure the table sales_transactions is successfully created — this will be used in Power BI

2. 📥 **Connect Power BI to MySQL**
Open Power BI Desktop

Click Home → Get Data → MySQL Database

Enter:

Server: localhost or your IP

Database: sales_db

Provide your MySQL username/password

Click Connect to load tables like sales_transactions, products, markets, etc.

3. 📎 **Import Excel File**
Go to Home → Get Data → Excel

Select transactions.xlsx

Load the required sheet or table

📌 This file contains additional transaction data to compare/merge with the sales_transactions table

4. 🧹 **Perform ETL Using Power Query**
Click Transform Data

Clean both SQL and Excel tables:

Remove duplicates or nulls

Rename columns for consistency (especially between the Excel and MySQL tables)

Change data types

Create relationships if needed (e.g., matching transaction_id, product_id)

Optionally, merge or append the sales_transactions and Excel transactions if they contain similar or complementary data

5. 🔗 **Data Modeling**
Create relationships between:

sales_transactions (from MySQL)

transactions (from Excel)

Lookup tables like products, customers, markets

Use the Manage Relationships tool in Power BI

6. 📈 **Create Visualizations**
Visuals included in this dashboard:

KPI cards (Total Sales, Profit, Orders)

Bar charts (Sales by Product, Category, Region)

Line chart (Monthly sales trend)

Donut chart (Market contribution)

Table comparing SQL vs Excel transactions (optional)

7. 🧮 **Create DAX Measures**
Sample measures used:
dax

Total Sales = SUM(Sales[Revenue])
Total Profit = SUM(Sales[Profit])
Total Orders = COUNTROWS(Sales)
Profit Margin = DIVIDE([Total Profit], [Total Sales])

8. 📊 **Final Dashboard Layout**
Interactive slicers: Date, Region, Product Category

Clean layout using grid system and card visuals

Table comparing MySQL transactions with Excel file entries

📤 Publishing
Publish the .pbix file to Power BI Service (optional)

Export to PDF or share via Power BI workspace

📌 Notes
Ensure MySQL ODBC connector is installed

MySQL server must be running when opening the dashboard

Excel file transactions.xlsx must be in the same path (or re-browse if moved)

🧑‍💻 Author
Sundram
Power BI Developer | Data Analyst

