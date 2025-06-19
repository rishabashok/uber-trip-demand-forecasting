# Uber Trip Demand Forecasting (Jan–Feb 2015)
This project involves predicting daily Uber trip demand using machine learning (Random Forest, XGBoost, Ensemble models) and presenting insights via an interactive Power BI dashboard.

## Project Overview

- **Goal:** Forecast daily Uber trip volume in New York for January–February 2015.
- **Approach:** Clean the dataset, engineer lag/rolling features, build ML models, evaluate performance using MAPE, and visualize results.
- **Tools Used:** Python (Pandas, Sklearn, XGBoost), Power BI

---

## Dataset

- File used: `Uber-Jan-Feb-FOIL.csv`
- Source: [NYC TLC FOIL Uber data](https://data.cityofnewyork.us/)
- Key columns:
  - `date` — day of record
  - `dispatching_base_number` — Uber base identifier
  - `active_vehicles` — vehicles active on that date
  - `trips` — total number of trips taken that day

---

## Machine Learning Models

| Model           | Description                         | Avg MAPE |
|----------------|-------------------------------------|----------|
| Random Forest   | Tree-based ensemble regressor        | 7.14%    |
| XGBoost         | Gradient boosting algorithm          | 8.27%    |
| Ensemble (avg)  | Combined RF & XGB predictions        | 7.36%    |

### Features Engineered
- Day of week
- Is weekend flag
- Lag features (1-day, 2-day)
- Rolling mean (3-day, 7-day)



## Residual Analysis

Residuals were plotted to check model bias and error stability.  
- Random Forest: Stable with one large spike
- XGBoost: Higher variance in residuals

---

## Power BI Dashboard

### What it shows:
- Actual vs Predicted trips (by model)
- Residuals over time
- Average trips by weekday
- Fully styled with slicers and titles

### 📂 Files included:
- `Uber_Trip_Analysis.ipynb` – Full Jupyter notebook (Python)
- `forecast_results.csv` – Model output for dashboard
- `daily_summary.csv` – Processed data for visuals
- `Uber_Trip_Dashboard_Rishab.pdf` – Dashboard export (preview)

![Dashboard Preview](C:\Users\rishab\Pictures\Screenshots\Screenshot 2025-06-19 234329.png)



## Key Takeaways

- Random Forest provided the most stable and accurate forecasts.
- Weekends (Saturday) showed highest average trips.
- Forecasts improved using lag + rolling features.

---

## Author

**Rishab Ashok**  
Data Analyst Intern | Python + Power BI Enthusiast_  
Connect on [LinkedIn](https://www.linkedin.com/in/rishab-ashok-655932354/)




