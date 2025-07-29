
# SANTANU EV Geographic Market Segmentation & Forecasting (India)

This project performs **state-wise market analysis** and **electric vehicle (EV) sales forecasting** across India using data from 2014 to 2024. It includes **clustering**, **geographic visualizations**, and a powerful **XGBoost-based time-aware regression model** to predict future EV sales.

---

## Project Objectives

- Analyze the Indian EV market based on **state-wise and category-wise** adoption trends.
- Identify **high-potential regions** and vehicle segments (2W, 3W, 4W, buses, others).
- Use **machine learning (XGBoost)** to forecast future EV sales (e.g., for Jan 2025).
- Provide data-driven recommendations for **EV startups and policy planning**.

---

## Contents

| Folder/File                  | Description                                 |
|-----------------------------|---------------------------------------------|
| `EV_Dataset.csv`            | Cleaned dataset: monthly EV sales per state/category |
| `EV_Segmentation_Analysis.ipynb` | EDA, clustering, choropleth maps, XGBoost model |
| `india.geojson`             | GeoJSON file used for state-wise maps       |
| `README.md`                 | Project overview (this file)                |

---

##  Tools & Libraries Used

- **Python** (Pandas, NumPy, Matplotlib, Seaborn)
- **Machine Learning**: XGBoost, scikit-learn
- **Geospatial Analysis**: GeoPandas
- **Visualization**: Choropleth maps, Feature importance plots

---

##  ML Model Summary: XGBoost

- Features used:
  - `State`, `Vehicle_Category`, `Year`, `Month`
  - `Lag_1`, `Lag_2`, `Rolling_Mean_3`
- Target: `EV_Sales_Quantity` (log-transformed)
- R² Score: **0.64**
- RMSE: **~0.79 (log scale)**

> Predicts monthly EV sales with solid accuracy, especially in top-performing states like Maharashtra, Karnataka, and Tamil Nadu.

---

##  Clustering & Segmentation

- Performed **K-Means Clustering** on cumulative sales by state and vehicle type.
- Identified **4 regional clusters** based on EV adoption behavior.
- Mapped clusters using **choropleth maps** via GeoPandas.

---

##  Forecast Example (Jan 2025)

> Forecasted EV 2W sales for **Tamil Nadu** in **Jan 2025** using lag-based input features.

