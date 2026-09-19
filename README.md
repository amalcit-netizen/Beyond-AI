# Machine Learning Applications in E-Commerce: National Day Demand Forecasting & Inventory Optimization 📊🇸🇦
## Executive Summary
This project is part of the **Machine Learning Applications in E-Commerce** program (تطبيقات تعلّم الآلة في التجارة الإلكترونية) organized by **Beyond AI Initiative** in collaboration with **Zid**.

The goal of this project is to leverage historical e-commerce transactional data from Zid's platform to build a predictive machine learning pipeline. The model forecasts product demand during the high-volume Saudi National Day season and optimizes inventory planning to prevent stockouts and overstocking.

---

## Project Architecture & Workflow
1. **Data Integration & Cleaning:** Merged `orders.csv`, `products.csv`, and `calendar.csv` datasets, processed missing values, and calculated revenue dynamically (`Quantity * Unit Price * (1 - Discount %)`).
2. **Exploratory Data Analysis (EDA):** Identified seasonal purchasing trends and demand spikes occurring 2 to 3 weeks prior to Saudi National Day (Sept 23).
3. **Feature Engineering:** Extracted temporal features (day, month, year, day of week, weekend flags) and encoded categorical variables (`product_id`, `city`, `channel`).
4. **Machine Learning Modeling:** Trained a **Random Forest Regressor** to predict daily order quantities per product.
5. **Business Intelligence & Recommendations:** Calculated recommended stock buffer (25% safety stock) and identified the optimal marketing launch window.

---

## Model Performance
* **Model:** Random Forest Regressor
* **Mean Absolute Error (MAE):** 0.61
* **Root Mean Squared Error (RMSE):** 0.73

---

## Strategic Business Insights
* **Recommended Marketing Launch Window:** September 1st – September 5th (captures the initial 2-3 week pre-National Day demand curve).
* **Inventory Allocation:** Stock levels should be scaled up by **25% above historical averages** for core National Day merchandise (flags, national dress, green LED accessories, gifts).

---

## Tech Stack & Tools
* **Programming Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn
* **Data Sources:** Zid E-Commerce Platform Datasets
