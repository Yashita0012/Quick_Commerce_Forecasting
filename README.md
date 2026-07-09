# 🛒 Quick Commerce Demand Forecasting & Inventory Optimization

## 📌 Project Overview

Quick commerce companies such as Blinkit, Zepto, and Swiggy Instamart rely on accurate demand forecasting to maintain optimal inventory levels, reduce stock-outs, and improve customer satisfaction.

This project explores customer purchasing behavior using the Instacart Market Basket Analysis dataset and performs extensive Exploratory Data Analysis (EDA) to uncover demand patterns that can support inventory optimization and future forecasting models.

> **Note:** The original Instacart dataset does not contain store-level information. For quick commerce simulation, virtual dark stores were randomly assigned to orders for analytical purposes.

---

## 🎯 Business Objective

The primary objectives of this project are to:

* Analyze customer purchasing behavior.
* Identify peak shopping hours and demand trends.
* Discover high-demand products and departments.
* Measure customer reorder behavior.
* Generate business insights for inventory planning.
* Prepare a clean time-series dataset for demand forecasting.

---

## 📂 Dataset

**Dataset:** Instacart Market Basket Analysis

The project uses the following files:

* `orders.csv`
* `order_products__prior.csv`
* `products.csv`
* `aisles.csv`
* `departments.csv`

After merging these datasets, a unified transactional dataset was created for analysis.

---

## 🛠️ Tech Stack

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## 📊 Data Preparation

The following preprocessing steps were performed:

* Merged all relational tables into a single dataframe.
* Checked data types and dataset structure.
* Identified missing values.
* Verified duplicate records.
* Simulated dark-store IDs for quick commerce analysis.
* Prepared the dataset for exploratory analysis.

---

## 📈 Exploratory Data Analysis

The EDA focused on understanding customer purchasing behavior and product demand.

### Analysis Performed

* Order distribution by hour of the day
* Order distribution by weekday
* Top-selling products
* Top-performing aisles
* Department-wise reorder rate
* Basket size distribution
* Days between consecutive orders
* Product reorder behavior
* Store-wise order distribution (simulated)
* SKU demand distribution
* Correlation analysis

---

## 💡 Business Insights

### 1. Peak Shopping Hours

Customer purchases are concentrated during specific hours of the day, indicating periods where inventory replenishment and delivery resources should be prioritized.

---

### 2. High Reorder Categories

Departments such as fresh produce and daily essentials demonstrate significantly higher reorder rates, suggesting strong customer loyalty and the need for higher safety stock.

---

### 3. Product Demand Concentration

A relatively small number of products account for a large share of total orders, highlighting the importance of prioritizing these fast-moving SKUs in inventory planning.

---

## 📊 Data Characteristics

* Large-scale transactional dataset with millions of purchase records.
* Highly skewed demand distribution.
* More than half of SKU-date observations contain zero demand after time-series preparation.
* Demand follows a long-tail distribution with a few extremely popular products.

---

## 📁 Project Structure

```text
Quick-Commerce-Demand-Forecasting/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   └── 01_EDA.ipynb
│
├── images/
│
├── README.md
│
└── requirements.txt
```

---

## 🚀 Current Progress

* ✅ Data Collection
* ✅ Data Cleaning
* ✅ Data Integration
* ✅ Feature Preparation
* ✅ Exploratory Data Analysis
* ⏳ Time Series Dataset Construction
* ⏳ Feature Engineering
* ⏳ Demand Forecasting using XGBoost
* ⏳ Deep Learning (LSTM)
* ⏳ Streamlit Dashboard

---

## 📌 Future Work

The next phase of the project includes:

* Building a daily demand time-series dataset.
* Creating lag and rolling statistical features.
* Training an XGBoost demand forecasting model.
* Comparing forecasting performance with an LSTM model.
* Developing an interactive Streamlit dashboard for inventory monitoring.

---

## 📬 Author

**Yashita Kumari**

Aspiring Data Analyst | SQL | Python | Power BI | Machine Learning

Passionate about solving real-world business problems using data-driven insights.
