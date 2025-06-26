# 📦 Vendor Insights & Profitability Analysis

An end-to-end data analytics project to analyze vendor performance and improve business decision-making for a retail company.

## 🚀 Project Highlights

- ⚙️ Automated Data Ingestion into a SQLite database using Python, Pandas, and SQLAlchemy  
- 🧮 SQL-driven Data Preparation to compute key vendor performance metrics (sales, profit, margins, turnover)  
- 📊 Exploratory Data Analysis (EDA) using Python for outlier detection, trend identification, and data profiling  
- 💰 Profitability Analysis based on Gross Profit, Profit Margins, Inventory Turnover, and Vendor-wise KPIs  
- 📈 Interactive Excel Dashboard built for stakeholders

## 🧠 Business Problem

The company (a retailer) wants to:

- Identify underperforming vendors that may need promotional or pricing support  
- Understand which products are most and least profitable  
- Analyze the impact of bulk purchasing on cost efficiency  
- Detect inventory inefficiencies and high holding costs  
- Reduce vendor dependency and supply chain risk


## 🎯 Goal of the Project

Use real sales and vendor data to:

- Clean and organize the data  
- Analyze vendor and product performance  
- Build a dynamic Excel dashboard  
- Deliver actionable business insights


## 🔄 Workflow

1. Understand the Business Problem  
2. Collect Raw Data from CSV Files  
3. Clean and Prepare Data Using SQL  
4. Merge and Aggregate Vendor Data  
5. Load Aggregated Data into Jupyter Notebook  
6. Perform EDA using Python  
7. Export Final Dataset to Excel  
8. Create Interactive Dashboard in Excel


## 🧰 Tools & Technologies

- Python – Pandas, SQLite, SQLAlchemy  
- SQL – CTEs, JOINs, Aggregations  
- Excel – Dashboarding (Pivot Tables, Charts, Slicers)  
- Jupyter Notebook – EDA & Analysis


## 🛠️ Data Ingestion Scripting

A Python script automatically loads all raw CSV files into a SQLite database using Pandas and SQLAlchemy, while logging the process and tracking ingestion time.

### Components Used:

- **SQLite:**  
  - Lightweight `.db` file to store structured tables  
  - Used to store and query data efficiently  

- **Pandas:**  
  - Read and transform `.csv` files  
  - Used `pd.read_csv()` and `df.to_sql()` for ingestion

- **SQLAlchemy:**  
  - Created a database engine: `create_engine('sqlite:///inventory.db')`  
  - Acts as a bridge between Pandas and SQLite

### 🔍 Logging:
A log file is generated at `logs/ingestion_db.log` to track:
- Which files were loaded  
- When they were ingested  
- Total time taken  
- Any ingestion issues (extendable for error logs)


## 📊 Key EDA Insights & Findings

- ❌ Negative gross profit and zero sales indicate loss-making or obsolete inventory  
- 📈 High standard deviations reveal price and freight cost outliers  
- 🔁 Stock turnover ranges from 0 to 274.5 → wide variation in product movement

### 🧹 Filters Applied:
- Removed:
  - Gross Profit ≤ 0  
  - Profit Margin ≤ 0  
  - Total Sales Quantity = 0  

### 📉 Correlation Highlights:
- 💸 Weak link: Purchase Price vs. Sales/Gross Profit  
- 🔄 Strong link: Purchase Quantity vs. Sales Quantity  
- 📉 Negative link: Profit Margin vs. Sales Price


## 🧪 Research Insights

1. **198 high-margin, low-sales brands** → Good candidates for promotions  
2. **Top 10 vendors = 65.69% of purchases** → High vendor dependency risk  
3. **Bulk buying = 72% unit cost savings** → Cost-effective purchase strategy  
4. **₹2.71 Cr in unsold inventory** → Suggests clearance or better stock planning  
5. **Low-performing vendors have higher margins** but lower sales → Pricing or market issue  
6. **Statistical test confirms**: Profit margins differ significantly between top and low-performing vendors



## ✅ Final Recommendations

- 💡 Re-evaluate pricing for low-volume, high-margin products  
- 🧩 Diversify vendor partnerships to reduce supply chain risks  
- 📦 Use bulk purchasing where it drives cost savings  
- 🧹 Optimize slow-moving inventory through clearance or reorder planning  
- 📢 Enhance marketing for low-performing vendors to improve sales



This project demonstrates how data-driven insights can improve vendor relationships, purchasing strategy, and overall profitability for retail businesses.

