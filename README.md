# 🛒 Quick Commerce Demand Forecasting & Inventory Optimization

## 📖 Overview

Quick commerce platforms such as **Blinkit, Zepto, Swiggy Instamart, and BigBasket Now** rely on accurate demand forecasting to ensure product availability while minimizing excess inventory.

This project builds an end-to-end demand forecasting pipeline using the **Instacart Market Basket Analysis** dataset. The project focuses on understanding customer purchasing behavior, engineering forecasting features, and building an XGBoost-based demand forecasting model to support inventory optimization.

---

# 🎯 Business Problem

Retailers frequently face two major inventory challenges:

* **Stock-outs**, resulting in lost sales and poor customer experience.
* **Overstocking**, leading to unnecessary inventory holding costs.

The objective of this project is to forecast future product demand so inventory can be replenished proactively and efficiently.

---

# 📂 Dataset

**Source:** Instacart Market Basket Analysis (Kaggle)

### Files Used

* orders.csv
* order_products__prior.csv
* products.csv
* aisles.csv
* departments.csv

The datasets were merged into a single analytical dataset containing customer orders, product information, department information, and purchasing behavior.

> **Note:** The original Instacart dataset does not contain store-level information. This project focuses on product-level demand forecasting.

---

# 🛠 Tech Stack

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* XGBoost
* Jupyter Notebook

---

# 📊 Data Preparation

The following preprocessing steps were performed:

* Merged multiple relational datasets.
* Performed data quality checks.
* Identified missing values.
* Removed duplicate records.
* Conducted exploratory data analysis.
* Constructed a product-level daily demand time series.
* Engineered forecasting features.

---

# 📈 Exploratory Data Analysis

The project investigates customer purchasing behavior through comprehensive exploratory analysis.

### Key Analyses

* Order distribution by hour of day
* Order distribution by weekday
* Top-selling products
* Top-performing aisles
* Department-wise reorder rate
* Basket size distribution
* Days since previous order
* Product reorder behavior
* Product demand distribution
* Correlation analysis

---

# 💼 Business Questions Solved

## 1. When do customers place the most orders?

Understanding peak ordering hours helps optimize workforce scheduling and inventory replenishment.

---

## 2. Which departments have the highest reorder rates?

Identifies product categories with strong customer loyalty that require higher inventory availability.

---

## 3. Which products generate the highest demand?

Highlights fast-moving SKUs that should receive priority during inventory planning.

---

# ⚙️ Feature Engineering

The forecasting model uses multiple time-series features, including:

* Day of Week
* Month
* Day of Year
* Lag-1 Demand
* Lag-3 Demand
* Lag-7 Demand
* Lag-14 Demand
* 7-Day Rolling Mean
* 14-Day Rolling Mean
* 7-Day Rolling Standard Deviation

These features capture demand trends, seasonality, and short-term purchasing patterns.

---

# 🤖 Model

The final forecasting model was built using **XGBoost Regressor**.

XGBoost was selected because it:

* Handles nonlinear relationships effectively.
* Performs well on sparse demand data.
* Trains significantly faster than deep learning models.
* Produces interpretable feature importance.
* Is widely adopted for structured retail forecasting problems.

---

# 📊 Model Performance

| Metric                                |      Score |
| ------------------------------------- | ---------: |
| Mean Absolute Error (MAE)             |   **0.55** |
| Root Mean Squared Error (RMSE)        |   **1.98** |
| Mean Absolute Percentage Error (MAPE) | **40.90%** |

### Performance Interpretation

The XGBoost model achieved a low Mean Absolute Error of **0.55 units**, indicating that demand predictions were generally close to actual demand.

Although the MAPE appears relatively high, the dataset contains a large number of zero- and low-demand observations. Percentage-based metrics tend to overestimate forecasting error under such conditions. Therefore, MAE and RMSE provide a more reliable assessment of forecasting performance.

---

# 📊 Key Business Insights

### 📌 Peak Shopping Hours

Customer demand is concentrated during specific hours of the day, suggesting that staffing and inventory replenishment should be prioritized during peak periods.

---

### 📌 High Reorder Categories

Essential product categories exhibit significantly higher reorder rates, indicating consistent customer demand and the need for higher safety stock.

---

### 📌 Fast-Moving Products

A relatively small number of products contribute disproportionately to total demand. Prioritizing these high-demand SKUs can reduce stock-outs and improve product availability.

---

### 📌 Demand Characteristics

The dataset exhibits highly intermittent demand, with many product-day combinations recording zero or very low sales. This behavior reflects real-world retail demand patterns and motivated the use of feature-based machine learning for forecasting.

---

# 📁 Project Structure

```text
Quick-Commerce-Demand-Forecasting/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_EDA.ipynb
│   ├── 02_Feature_Engineering.ipynb
│   └── 03_XGBoost_Forecasting.ipynb
│
├── images/
│
├── README.md
│
└── requirements.txt
```

---

# 🚀 Future Improvements

* Build an interactive Streamlit dashboard.
* Integrate Power BI dashboards for business reporting.
* Incorporate promotional and pricing features.
* Explore hierarchical demand forecasting.
* Evaluate additional forecasting algorithms using real timestamped retail datasets.

---

# 📚 Key Skills Demonstrated

* Data Cleaning
* Data Wrangling
* Exploratory Data Analysis
* Feature Engineering
* Time Series Forecasting
* Machine Learning
* XGBoost
* Model Evaluation
* Business Insight Generation
* Inventory Analytics

---

# 👩‍💻 Author

**Yashita Kumari**

**Aspiring Data Analyst | SQL | Python | Power BI | Machine Learning**

Passionate about transforming data into actionable business insights through analytics, visualization, and predictive modeling.
