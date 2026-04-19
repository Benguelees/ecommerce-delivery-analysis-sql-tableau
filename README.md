# 📦 E-Commerce Delivery & Sales Analysis

## 🎯 Business Problem

An e-commerce company is evaluating whether to expand its technology product line.

Key questions:
- Is there strong and sustainable demand for tech products?
- What drives delivery performance and customer satisfaction?

👉 Objective: Deliver actionable insights to support a data-driven expansion decision.

**🔑 Key Takeaway**

Strong demand for tech products is offset by declining revenue after 2018 Q1 and significant delivery delays — expansion should focus on mid-range products while improving operational efficiency.

---

## 📊 Dataset

- Source: Magist e-commerce dataset  
- ~100,000 orders  
- Time period: 2016–2018  
- Data includes: orders, products, sellers, customers, payments, reviews  

---

## ⚙️ Tools & Skills

- SQL (data cleaning, joins, aggregations)
- Tableau (dashboarding & storytelling)
- Data Analysis (EDA, business insights)

---

## 🔍 Key Insights

### 📦 Delivery Performance

![Delivery Performance](images_delivery_performance.png)

- ~92% of orders delivered on time  
- Delayed orders take ~3x longer (~30 vs ~10 days)  
- Delivery delays strongly impact customer experience  

---

### 📈 Revenue Trends

![Revenue Trends](revenue_trends.png)

- Rapid growth from 2017 → early 2018  
- Peak reached in 2018 Q1  
- Decline afterwards introduces uncertainty  

⚠️ Important:
- Root cause cannot be confirmed with available data  
- Possible factors: competition, pricing, marketing, operations  

---

## 📊 Summary Insights

- Strong demand for technology products  
- Customers are price-sensitive → mid-range performs best  
- Delivery is generally reliable, but delays are critical  
- Growth is not clearly stable → risk in expansion  

---

## 💼 Business Recommendation

**Recommendation:**  
Proceed with expansion in the technology category, focusing on mid-range products, while addressing key operational risks.

### Strategic Actions

- Expand **mid-range tech products**, where demand and volume are strongest  
- Reduce **extreme delivery delays**, which significantly impact customer experience  
- Improve logistics consistency to maintain high on-time delivery performance (~92%)

### ⚠️ Key Risks

- Revenue decline after 2018 Q1 introduces uncertainty in demand sustainability  
- Root cause of decline is unclear (potential factors: competition, pricing, marketing, operations)

**Next Step:**  
Validate revenue trends and investigate cost and market dynamics before scaling aggressively.
---

## 💻 SQL Analysis (Core Queries)

### 1. Delivery Performance by Order Status

```sql
SELECT
    order_status,
    ROUND(AVG(DATEDIFF(order_delivered_customer_date, order_purchase_timestamp)), 1) AS avg_delivery_days
FROM orders
GROUP BY order_status;

**Insight:** Delayed orders take ~3x longer than on-time deliveries, highlighting a significant delivery performance gap.

SELECT
    YEAR(order_purchase_timestamp) AS year,
    QUARTER(order_purchase_timestamp) AS quarter,
    ROUND(SUM(payment_value), 0) AS total_revenue
FROM orders o
JOIN payments p ON o.order_id = p.order_id
GROUP BY year, quarter
ORDER BY year, quarter;

**Insight:** Revenue grows steadily until 2018 Q1, followed by a decline — introducing uncertainty in demand sustainability.

SELECT
    CASE
        WHEN price < 50 THEN 'Low'
        WHEN price BETWEEN 50 AND 150 THEN 'Mid'
        ELSE 'High'
    END AS price_segment,
    COUNT(*) AS total_orders
FROM order_items
GROUP BY price_segment;

**Insight:** Mid-range products generate the highest order volume, indicating strong price sensitivity.
