# 📊 Customer Shopping Behavior Analysis  
### End-to-End Data Analytics Portfolio Project (Python | PostgreSQL | Power BI)

---

## 🔍 Project Overview
This project analyzes **customer shopping behavior** to uncover insights into purchasing patterns, customer demographics, product performance, and revenue drivers.  
The goal is to simulate a **real-world data analytics workflow**—from raw data preprocessing to SQL-based analysis and interactive dashboard visualization.

---

## 🎯 Business Objectives
The project aims to answer key business questions such as:
- How does revenue vary by gender and age group?
- Do subscribed or repeat customers spend more?
- Which products and categories perform best?
- How effective are discounts and shipping options?
- What payment methods do customers prefer?

---

## 🛠️ Tools & Technologies
- **Python (Pandas, SQLAlchemy)** – Data cleaning, preprocessing, feature engineering  
- **PostgreSQL** – Data storage and analytical SQL queries  
- **Power BI** – Interactive dashboard and business insights  

---

## 🧹 Data Preprocessing (Python)
The raw dataset was cleaned and prepared using Python. Key steps included:

- Loading and inspecting data (`info()`, `describe()`, null checks)
- Standardizing column names (lowercase, snake_case)
- Handling missing values in `review_rating` using **median by category**
- Renaming columns for clarity
- Feature engineering:
  - **Age Group** using fixed bins (Young, Adult, Middle-aged, Senior)
  - **Purchase Frequency (Days)** mapped from textual frequency values
- Removing redundant columns (`promo_code_used`)

### Example Feature Engineering:
``python
bins = [0, 25, 40, 55, 100]
labels = ['Young', 'Adult', 'Middle-aged', 'Senior']
df['age_group'] = pd.cut(df['age'], bins=bins, labels=labels)

## 🗄️ Database & SQL Analysis
After preprocessing, the cleaned dataset was loaded into a PostgreSQL database using SQLAlchemy.  
SQL was used to perform analytical queries focused on revenue, customer segmentation, product performance, and discount effectiveness.

## 📌 Key Analytical Questions & SQL Queries
- Total revenue by gender  
- High-spending customers who used discounts  
- Top 5 products by average review rating  
- Purchase behavior by shipping type  
- Spending comparison between subscribed and non-subscribed customers  
- Products with highest discount usage  
- Customer segmentation (New, Returning, Loyal)  
- Top products within each category  
- Subscription behavior of repeat buyers  
- Revenue contribution by age group

## 📊 Power BI Dashboard
An interactive Power BI dashboard was created to visualize key business metrics and trends.

### Dashboard Highlights:
- Revenue breakdown by gender and age group
- Subscription vs non-subscription spending
- Top-performing products and categories
- Discount usage patterns
- Preferred payment methods

📷 *Dashboard preview available in the `/dashboard` folder.*

## 💡 Key Insights
- Subscribed and loyal customers contribute significantly higher revenue
- Discounts increase purchase frequency but not always average order value
- Certain categories dominate revenue despite fewer purchases
- Middle-aged and adult customers are the most profitable segments

## 📁 Project Structure
customer-shopping-behavior-analysis/
│
├── data/
│   └── customer_shopping_behavior.csv
├── notebooks/
│   └── data_cleaning.ipynb
├── sql/
│   └── analysis.sql
├── dashboard/
│   └── powerbi_dashboard.png
└── README.md

## ▶️ How to Run This Project
1. Clone the repository
2. Run the Jupyter Notebook for data preprocessing
3. Load the cleaned data into PostgreSQL
4. Execute SQL queries for analysis
5. Open Power BI dashboard for visualization

## 🏁 Conclusion
This project demonstrates an end-to-end data analytics workflow involving data cleaning, SQL analysis, and dashboard creation.  
It reflects real-world analytical thinking and business-focused insights using industry-standard tools.
