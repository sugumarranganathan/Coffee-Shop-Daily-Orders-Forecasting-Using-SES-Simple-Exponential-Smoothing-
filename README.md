# Coffee Shop Daily Orders Forecasting Using SES (Simple Exponential Smoothing)

https://colab.research.google.com/drive/1wUDvJX-MNTUEOLAtxOhx8lJFIdDfLei5#scrollTo=PqkgUumyDGbF

## Project Overview

This project focuses on forecasting daily coffee shop orders using the Simple Exponential Smoothing (SES) model. The objective is to predict short-term customer demand based on historical order data and support operational planning, inventory management, and staffing decisions.

Simple Exponential Smoothing is a widely used time series forecasting technique that is suitable for datasets with no significant trend or seasonal pattern.

---

## Dataset Information

**Dataset Name:** Coffee Shop Orders Dataset

**Original Records:** 4,000 Customer Orders

**Processed Dataset:** Daily Order Counts

### Variables Used

| Variable | Description              |
| -------- | ------------------------ |
| Date     | Order Date               |
| Orders   | Number of Orders per Day |

---

## Project Objectives

* Analyze daily coffee shop order patterns.
* Forecast future customer demand.
* Evaluate forecasting performance using error metrics.
* Support inventory and workforce planning.

---

## Technologies Used

* Python
* Google Colab
* Pandas
* NumPy
* Matplotlib
* Statsmodels
* Scikit-Learn

---

## Methodology

### 1. Data Collection

The coffee shop transaction dataset containing 4,000 customer orders was loaded into Google Colab.

### 2. Data Preprocessing

* Converted Date column into datetime format.
* Aggregated individual transactions into daily order counts.
* Set Date as the index for time series analysis.
* Checked and handled missing values.

### 3. Exploratory Data Analysis

Daily order trends were visualized using line plots.

### Observation

* Daily orders ranged between approximately 20 and 55.
* Average daily demand remained around 34 orders.
* No significant upward or downward trend was observed.
* No clear seasonal pattern was detected.

---

## Model Used

### Simple Exponential Smoothing (SES)

SES forecasts future values by assigning higher importance to recent observations while retaining information from historical data.

### SES Formula

Forecast = α(Current Observation) + (1 − α)(Previous Forecast)

Where:

* α = Smoothing Parameter
* 0 ≤ α ≤ 1

---

## Model Training Results

| Parameter               |   Value |
| ----------------------- | ------: |
| Number of Observations  |      98 |
| Smoothing Level (Alpha) |  0.1684 |
| SSE                     | 4201.57 |
| AIC                     |  372.31 |
| BIC                     |  377.48 |
| AICC                    |  372.74 |
| Trend                   |    None |
| Seasonality             |    None |

---

## Model Performance

### Error Metrics

| Metric | Value |
| ------ | ----: |
| MAE    |  5.55 |
| RMSE   |  6.91 |

### Interpretation

* The average forecast error is approximately 5.55 orders.
* The model demonstrates good short-term forecasting performance.
* Forecast errors are relatively small compared to average daily demand.

---

## Actual vs Forecast Analysis

The forecast values closely follow the overall average demand level.

### Key Findings

* Actual orders fluctuate daily.
* SES smooths random fluctuations.
* The model captures the overall demand level effectively.
* Sudden peaks and dips are not explicitly predicted.

---

## Future Forecast (Next 7 Days)

| Date       | Forecast Orders |
| ---------- | --------------: |
| 2025-09-01 |           34.38 |
| 2025-09-02 |           34.38 |
| 2025-09-03 |           34.38 |
| 2025-09-04 |           34.38 |
| 2025-09-05 |           34.38 |
| 2025-09-06 |           34.38 |
| 2025-09-07 |           34.38 |

### Forecast Interpretation

The SES model predicts approximately 34 orders per day over the next week, indicating stable customer demand.

---

## Results

### Achievements

* Successfully aggregated transaction-level data into daily order counts.
* Built and trained a Simple Exponential Smoothing model.
* Evaluated forecasting accuracy using MAE and RMSE.
* Generated a 7-day future demand forecast.
* Provided business insights for operational planning.

---

## Business Insights

| Area                  | Insight                  |
| --------------------- | ------------------------ |
| Customer Demand       | Stable                   |
| Future Orders         | Approximately 34 per day |
| Inventory Planning    | Predictable              |
| Staffing Requirements | Consistent               |
| Business Risk         | Low                      |

---

## Conclusion

The Simple Exponential Smoothing (SES) model was successfully applied to forecast daily coffee shop orders. The dataset exhibited no significant trend or seasonality, making SES an appropriate forecasting method. The model achieved an MAE of 5.55 and an RMSE of 6.91, indicating satisfactory forecasting accuracy. The 7-day forecast suggests stable future demand of approximately 34 orders per day. The results demonstrate that SES is an effective tool for short-term demand forecasting and business planning in coffee shop operations.

---

## Prepared by

**Sugumar Ranganathan, M.B.A.,**
