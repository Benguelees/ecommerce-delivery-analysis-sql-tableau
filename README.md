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
![Delivery Performance](images_delivery_performance.png)

- Delivery reliability is high (~92% on-time), indicating stable logistics performance
- However, delays are severe (~3x longer), creating a disproportionate negative customer experience risk
- This suggests that improving delay handling (not overall delivery rate) is the highest-impact operational lever
- Delivery speed is a key driver of customer experience  

---

### 📈 Revenue Trends Over Time (Business Growth Analysis)

![Revenue Trends](revenue_trends.png)

- Revenue grew rapidly from 2017 to early 2018, indicating increasing market demand for tech products
- Peak reached in 2018 Q1  
- Revenue peaks in 2018 Q1 and declines afterwards
- Without additional data (costs, competition, marketing), the cause cannot be confirmed
- This signals a need for deeper investigation before making expansion decisions

---

## 📊 Summary Insights

- Tech products show strong market demand with clear growth until 2018
- Delivery performance is high (~92% on-time) but delays significantly impact experience
- Mid-range products outperform → customers are price-sensitive

## 💼 Business Recommendation
 
Based on the analysis:

- The tech category shows strong demand and growth potential
- Mid-range products perform best → pricing strategy is critical
- Delivery reliability is high, but delays have high impact

👉 Recommendation:
Focus expansion on mid-range tech products while prioritizing logistics improvements for delayed deliveries.

👉 Risk:
Revenue decline after 2018 suggests uncertainty — further validation is required before scaling.

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
