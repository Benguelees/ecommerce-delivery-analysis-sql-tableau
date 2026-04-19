# E-Commerce Delivery & Sales Analysis

## 📌 Problem

An e-commerce company is evaluating whether to expand its technology product line.  

The key challenge is to understand:  
- Is there strong and sustainable demand for tech products?  
- What factors influence delivery performance and customer satisfaction?  

This analysis aims to provide data-driven insights to support a strategic expansion decision.
---

## 📊 Dataset

* Source: Magist e-commerce database
* ~100,000 orders
* Time period: 2016–2018
* Multiple tables: orders, products, sellers, customers, payments, reviews

---

## ⚙️ Approach

* Cleaned and explored data using SQL
* Joined multiple tables to create analysis-ready datasets
* Analyzed:

  * product categories
  * pricing behavior
  * delivery times
  * customer reviews
* Built dashboards in Tableau for visualization

---

## 🔍 Key Insights

### 📦 Delivery Performance (Operational Insight)
![Delivery Performance](images/delivery_performance.png)

- ~92% of orders delivered on time  
- Delayed orders take significantly longer (~30 days vs ~10 days)  
- Delivery speed is a key driver of customer experience  

---

### 📈 Revenue Trends Over Time (Business Growth Analysis)

![Revenue Trends](images/revenue_trends.png)

- Strong growth from 2017 to early 2018  
- Peak reached in 2018 Q1  
- Decline after 2018 Q1 indicates potential market saturation or operational inefficiencies


---

### 📊 Summary Insights

- 📈 Strong demand for technology products (electronics, accessories)  
- 💰 Customers are highly price-sensitive → mid-range products perform best  
- ⏱️ Average delivery time ≈ 12.5 days  
- ❗ Delivery delays are **not strongly influenced by product size**  

---

## 📊 Visualizations

The Tableau dashboard includes:

* Demand by product category
* Revenue distribution by price range
* Delivery performance and delays

---

## 🛠 Tools

* SQL (MySQL)
* Tableau
* CSV data processing

---

## 📂 Project Structure

* `/sql` → SQL queries
* `/data` → exported CSV files
* `/tableau` → dashboards
* `/images` → screenshots

---

## 🚀 Outcome

This project demonstrates how data analysis can support **business decisions**, specifically:

* market expansion strategy
* pricing strategy
* delivery optimization

---

## 📌 Next Steps

* Analyze repeat customers
* Compare tech vs non-tech sellers in more detail
* Build predictive models for delivery delays
