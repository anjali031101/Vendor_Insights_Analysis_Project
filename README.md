# Vendor_Insights & Profitable Analysis
Create an end to end data analytics project

Business Problem:
The company(Retailer) wants to find out:

- Which vendors (suppliers) are performing well or not & may need discounts or ads
- Which products give high or low profit
- Whether buying in bulk is actually saving money (per unit cost)
- If we are keeping too much stock (and paying for storage)
- Which vendors we can depend on more (or less)

Goal of the Project:
Use real sales and vendor data to:
- Clean and organize the data
- Analyze vendor performance
- Create a simple Excel dashboard
- Help the company take better decisions

Workflow:
1.Understand the Business Problem
2.Collect Raw Data from Database
3.Clean and Prepare Data Using SQL
4.Merge and Aggregate Vendor Data
5.Load Aggregated Data into Jupyter Notebook
6.Perform EDA using Python
7.Export Final Dataset to Excel
8.Create Interactive Dashboard in Excel

Steps:
1. Wrote a Python script to automatically load all raw CSV files into a SQLite database using Pandas and SQLAlchemy, while logging the process and tracking ingestion time.
Used:
# SQLITE: A simple database stored in a single .db file.
-Used it to store tables(csv files)  and run SQL queries on them later.
-Created a file called inventory.db using SQLite. All the data from .csv files gets stored in this file.
# Pandas: Powerful tool to work with Tabular Data
- To read CSV files, turn them into dataframes, and manipulate them.
- Used pandas.read_csv() to load each .csv file and used df.to_sql() to send it to the database.
#SQLAlchemy: A Python toolkit that connects your code to databases.
- Created an engine using create_engine('sqlite:///inventory.db') so that Pandas knows where to send the data.
  
#During the ingestion process, a log file is created 
log tracks the progress of each CSV file being ingested into the SQLite database. It helps monitor:
Which files were loaded
When they were ingested
Total time taken
If anything went wrong (can also be extended to log errors)


