# 🛒 Brazilian E-Commerce Data Analysis (Power BI + Python)

This project focuses on analyzing the **Brazilian E-Commerce Public Dataset (Olist)** by integrating **data cleaning, preprocessing, and feature engineering in Python**, followed by **interactive dashboards in Power BI**.  

The aim is to generate **business insights** into customer behavior, sales, delivery performance, and product categories.  

---

## 📂 Project Structure
- `code/` → Python scripts for data cleaning, merging, and preprocessing  
- `datasets/` → Original CSVs (6–7 provided datasets)  
- `master_dataset.csv` → Final consolidated dataset used for Power BI  
- `dashboard.pbix` → Power BI dashboard file  
- `README.md` → Project documentation  

---

## 🛠️ Tech Stack
- **Python** → pandas, numpy, matplotlib, seaborn  
- **Power BI** → Interactive dashboards & visualizations  
- **Jupyter Notebook** → Exploratory data cleaning & feature engineering  

---

## 🔧 Data Preparation (Python)
1. **Dataset Merging**  
   - Combined multiple datasets (`orders`, `customers`, `products`, `sellers`, `reviews`, etc.)  
   - Created a **master dataset** with all relevant fields for analysis.  

2. **Data Cleaning**  
   - Removed invalid rows (negative prices/quantities).  
   - Converted timestamps to datetime format.  
   - Filled missing values:  
     - Product attributes → median/zero  
     - Reviews → `"No Comment"` / `"No Title"`  
     - Product category translation → Portuguese fallback  

3. **Feature Engineering**  
   - `order_year_month` → For trend analysis  
   - `order_processing_time_hours` → Purchase → Approval gap  
   - `actual_delivery_time_days` → Carrier → Customer delivery time  
   - `delivery_diff_days` → Early vs late delivery  
   - `delivery_status` → On-time, late, canceled, pending  
   - `purchase_month`, `purchase_day_of_week`, `purchase_hour` → Seasonal analysis  
   - `item_total_revenue` → Price + freight value  

---

## 📊 Power BI Dashboard
Key visuals included:  
- **Revenue by Product Category**  
- **Monthly Sales & Growth Trends**  
- **Delivery Status Breakdown (on-time vs late vs canceled)**  
- **Customer Demographics (region, city)**  
- **Top Sellers & Products**  
- **Customer Review Scores vs Revenue**  

---

## 🚀 Insights
- Clear **seasonal sales patterns** across months and days of the week  
- **Delivery performance** strongly affects review scores  
- Certain product categories dominate sales (electronics, housewares, etc.)  
- Revenue is concentrated among a few **top-performing sellers**  
- Freight cost has a noticeable impact on total revenue and customer satisfaction  

---

## 📈 Next Steps
- Advanced predictive models (delivery delays, customer churn)  
- Sentiment analysis on review text  
- Deeper geo-spatial visualizations (city & state-level patterns)  

---

⚡ *This project combines the power of Python for robust data cleaning and feature engineering with Power BI for intuitive, business-friendly dashboards.*  
