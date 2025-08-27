## Retail-Demand-Forecasting
Business analysis of retail sales for Mumbai &amp; Delhi (Jun 2020–Sep 2022). Cleans and aggregates POS data, explores customer patterns and frequent product bundles, and builds daily sales forecasts (Holt’s, ARIMA, TBATS) to guide inventory, staffing, and promotion planning.

## 🚀 Overview

Goal: Provide insights to the company; understand clientele; predict sales using time-series models; produce daily forecasts with the best-fit approach.

Scope: Retail store data for Mumbai & Delhi (Jun 2020–Sep 2022), ~17,000 data points.
Method: Null handling → dataset compilation → spline interpolation → daily aggregation → stationarity tests (ADF/KPSS) → compare Holt’s, ARIMA, BATS/TBATS, Prophet → rolling forecasts.

🔢 Data
Source: Retail store sales dataset (Mumbai, Delhi; Jun 2020–Sep 2022).
Unit: Daily sales totals (aggregated from transactions).
Notes: Address missing values, duplicate dates, gaps; align to calendar before modeling.

🧪 Method & Model
Aggregation: transactions → daily sales.
Cleaning: handle nulls and irregular gaps; spline interpolation for continuity.
Stationarity: ADF and KPSS tests to assess differencing needs.
Model comparison: Holt’s method, ARIMA (including ARIMA(10,0,0)), BATS, TBATS, and FB Prophet evaluated via error metrics.
Chosen model: BATS/TBATS (best performance).

📈 Results
BATS/TBATS achieved the lowest error (MAPE ≈ 64%), a large improvement versus earlier baselines (~400% MAPE).
Findings and EDA provided practical learnings for time-series analysis on retail data.

✅ Forecast Usage
Use the daily forecasts to align inventory levels and schedule staff in advance of expected peaks and troughs.

⚠️ Limitations
MAPE is still higher than ideal for production use.
Exogenous drivers (company-specific or economic parameters) were not included.
Further improvement may come from stronger time-series variants or deep-learning/hybrid models.
