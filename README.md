# 🍕 Pizza Sales Data Analysis (SQL Project)

## 📌 Project Overview

This project focuses on analyzing a pizza sales dataset using SQL to extract meaningful business insights. The goal is to understand customer behavior, sales performance, and revenue trends to support data-driven decision making.

---

## 🎯 Objectives

* Analyze total orders and revenue
* Identify top-selling pizza types
* Understand category-wise performance
* Discover peak order times
* Generate business insights using SQL queries

---

## 🗂️ Dataset Description

The dataset includes the following tables:

* **orders** – order details with date & time
* **order_details** – quantity of pizzas per order
* **pizzas** – pizza size and price
* **pizza_types** – pizza name and category

---

## 🛠️ Tools & Technologies

* SQL (MySQL)
* Database Management System
* GitHub for version control

---

## 📊 Key Analysis Performed

* Total number of orders
* Total revenue generated
* Top 5 best-selling pizzas
* Revenue by pizza category
* Hourly order trends
* Top 3 pizzas per category (using window functions)

---

## 🔥 Sample SQL Query

```sql
SELECT 
    pizza_types.name,
    SUM(order_details.quantity * pizzas.price) AS revenue
FROM pizza_types
JOIN pizzas ON pizza_types.pizza_type_id = pizzas.pizza_type_id
JOIN order_details ON order_details.pizza_id = pizzas.pizza_id
GROUP BY pizza_types.name
ORDER BY revenue DESC;
```

---

## 📈 Key Insights

* Certain pizza categories generate higher revenue than others
* Peak sales occur during specific hours
* A small number of pizza types contribute to most revenue
* Customer preference trends can guide menu optimization

---

## 📁 Project Structure

```
pizza-sales-analysis/
│
├── data/
│   └── dataset files
│
├── sql/
│   └── queries.sql
│
├── README.md
```

---

## 🚀 How to Use

1. Import dataset into MySQL
2. Run SQL queries from `queries.sql`
3. Analyze outputs and insights

---

## 💡 Future Improvements

* Create Power BI dashboard
* Add data visualization
* Perform advanced analytics

---

## 🙌 Author

**Your Name**
Aspiring Data Analyst

---

## ⭐ If you like this project

Give it a star on GitHub!

