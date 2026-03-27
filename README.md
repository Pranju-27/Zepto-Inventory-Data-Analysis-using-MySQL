# 📊 End-to-End SQL Data Analytics Project on E-commerce Inventory (MySQL)

## 📌 Project Overview

This project demonstrates a complete data analysis workflow using a real-world e-commerce zepto dataset inspired by Zepto. The goal is to clean, analyze, and extract actionable business insights using MySQL.

---

## 🎯 Objectives

* Build a structured database from raw data
* Perform data cleaning and preprocessing
* Conduct exploratory data analysis (EDA)
* Solve business problems using SQL queries
* Generate insights for zepto and revenue optimization

---

## 🛠️ Tech Stack

* **Database:** MySQL
* **Tools:** MySQL Workbench / VS Code
* **Language:** SQL

---

## 📂 Dataset Description

The dataset contains e-commerce zepto details such as:

* Product Name
* Category
* Price (in paise)
* Stock Quantity
* Discount
* Availability

---

## ⚙️ Database Setup

Database created and structured in MySQL with a well-defined schema for handling e-commerce inventory data.

---

## 🧹 Data Cleaning

sql
UPDATE zepto
SET price = price / 100;

```

sql
DELETE FROM zepto
WHERE product_name IS NULL OR category IS NULL;
```

sql
DELETE t1 FROM zepto t1
JOIN zepto t2
ON t1.product_name = t2.product_name
AND t1.product_id > t2.product_id;

```

---

## 🔍 Exploratory Data Analysis (EDA)
- Analyzed total number of products
- Identified unique categories
- Evaluated product distribution across categories

---

## 📈 Business Analysis

sql
SELECT SUM(price * stock) AS total_zepto_value
FROM zepto;
```

sql
SELECT product_name, price
FROM zepto
ORDER BY price DESC
LIMIT 5;

```

sql
SELECT product_name, stock
FROM zepto
WHERE stock < 10;
```

sql
SELECT category, AVG(price) AS avg_price
FROM zepto
GROUP BY category;

```

sql
SELECT SUM(price * stock) AS estimated_revenue
FROM zepto;
```

---

## 📊 Key Insights

* Identified high-value products contributing most to zepto
* Detected low-stock items requiring restocking
* Analyzed category-wise product distribution
* Estimated total zepto value and potential revenue

---

## 🚀 Conclusion

This project highlights practical SQL skills including data cleaning, aggregation, and business analysis. It simulates real-world data analyst tasks and demonstrates the ability to transform raw data into meaningful insights.

---

## 📌 Future Improvements

* Build dashboard using Power BI / Tableau
* Add time-based sales analysis
* Implement advanced SQL (window functions)

---

## ⭐ If you found this useful, give it a star!
