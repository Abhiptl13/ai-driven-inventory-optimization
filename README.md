# AI-Driven Inventory Optimization Using Demand Forecasting and Machine Learning

## Research Overview

This research project explores how Artificial Intelligence and Machine Learning can be used to improve inventory management by reducing stockouts, minimizing overstocking, and enhancing demand forecasting accuracy.

The study was conducted using the Walmart Weekly Sales dataset and focuses on developing a lightweight, explainable, and cost-effective forecasting framework specifically designed for Small and Medium-Sized Enterprises (SMEs).

Unlike many enterprise-level forecasting systems that require significant computational resources, this research demonstrates that highly accurate forecasting and inventory optimization can be achieved using affordable and practical machine learning techniques that can run on standard hardware.

The proposed framework combines classical statistical forecasting, advanced machine learning models, and inventory planning strategies to provide actionable business insights for inventory decision-making.

---

## Research Objectives

The primary objectives of this study are:

* Improve demand forecasting accuracy for SMEs.
* Reduce inventory stockouts and excess inventory.
* Compare traditional statistical forecasting methods with machine learning approaches.
* Develop a lightweight and explainable forecasting framework.
* Convert forecasting outputs into practical inventory planning metrics.
* Demonstrate the real-world value of AI-driven inventory optimization.

---

## Key Contributions

This research introduces several important contributions:

### SME-Friendly Forecasting Framework

A lightweight and computationally efficient forecasting pipeline designed specifically for small and medium-sized enterprises.

### Multi-Scale Evaluation

The forecasting framework was evaluated across:

* Single Store Operations
* Multi-Store Retail Chains
* Fully Aggregated Enterprise-Level Demand

### Inventory Optimization Integration

Demand forecasts were transformed into:

* Safety Stock Calculations
* Reorder Point Calculations
* Inventory Planning Recommendations

### State-of-the-Art Forecasting Accuracy

The proposed XGBoost-based framework achieved forecasting accuracy significantly better than many approaches reported in existing literature.

---

## Dataset

### Walmart Weekly Sales Dataset

The project utilizes the Walmart Weekly Sales Dataset containing:

* Weekly sales data
* Holiday indicators
* Temperature data
* Fuel prices
* Consumer Price Index (CPI)
* Unemployment rates

The dataset provides realistic retail demand patterns and enables evaluation across multiple business scales.

---

## Data Engineering Pipeline

The forecasting workflow includes extensive feature engineering:

### Lag Features

Historical sales values from previous weeks:

* Lag 1
* Lag 2
* Lag 3
* Lag 4
* Lag 5
* Lag 6

### Rolling Statistics

Moving averages over:

* 2-week windows
* 3-week windows
* 4-week windows
* 5-week windows

### Calendar Features

* Month
* Week of Year

### External Economic Variables

* Holiday Events
* Temperature
* Fuel Price
* CPI
* Unemployment

---

## Models Evaluated

### Baseline Models

#### Naive Forecasting

Uses previous week's demand as the forecast.

#### Moving Average

Uses historical rolling averages to generate forecasts.

---

### Statistical Model

#### SARIMAX

Seasonal Auto-Regressive Integrated Moving Average with Exogenous Variables

Features:

* Time-series forecasting
* Seasonal pattern detection
* External variable integration

---

### Machine Learning Model

#### XGBoost Regressor

Chosen because it:

* Handles nonlinear relationships
* Supports mixed feature types
* Provides high forecasting accuracy
* Maintains computational efficiency
* Offers feature importance explanations

---

### Hybrid Forecasting Model

#### XGBoost + Random Forest

A two-stage forecasting architecture:

1. XGBoost generates primary forecasts.
2. Random Forest models residual errors.
3. Final prediction combines both outputs.

This hybrid architecture improves robustness while maintaining interpretability.

---

## Model Evaluation Metrics

Performance was measured using:

### Mean Absolute Error (MAE)

Measures average forecasting error.

### Root Mean Squared Error (RMSE)

Penalizes larger forecasting mistakes.

### Mean Absolute Percentage Error (MAPE)

Measures percentage forecasting accuracy.

---

## Results

### Forecasting Performance

The XGBoost model consistently outperformed:

* Naive Forecasting
* Moving Average
* SARIMAX

Across all business scales.

### Best Performance Achieved

| Dataset           | MAPE   |
| ----------------- | ------ |
| Store 1           | ~1.87% |
| Stores 1–10       | ~1.43% |
| Aggregated Demand | ~1.21% |

These results demonstrate exceptional forecasting accuracy while maintaining model simplicity and explainability.

---

## Inventory Optimization Framework

Forecast outputs were directly integrated into inventory management calculations.

### Safety Stock

Additional inventory maintained to reduce stockout risk.

### Reorder Point

Inventory threshold used to trigger replenishment.

### Forecast Error Analysis

Demand uncertainty was quantified using forecasting residuals.

This transforms forecasting outputs into practical business decisions.

---

## Scenario Analysis

A sensitivity analysis was performed to understand the impact of external variables on demand forecasts.

Example:

* Unemployment rates were artificially increased.
* Forecast changes were analyzed.
* Demand sensitivity was measured.

Results indicate that recent sales history and seasonality often have stronger short-term influence than macroeconomic indicators.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-Learn
* XGBoost
* Random Forest
* Statsmodels
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## Repository Structure

```text
ai-driven-inventory-optimization/
│
├── AI_research.pdf
├── Research_ARIMA&RF_MODEL.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Research Significance

This research demonstrates that small and medium-sized enterprises can successfully adopt Artificial Intelligence for inventory planning without requiring expensive infrastructure or large technical teams.

The proposed framework offers:

* High Forecast Accuracy
* Low Computational Cost
* Explainable Predictions
* Practical Inventory Planning
* Easy Deployment

making it suitable for real-world SME adoption.

---

## Future Work

Potential extensions include:

* Product-Level Forecasting
* Multi-Product Inventory Optimization
* Reinforcement Learning for Automated Ordering
* Cloud-Based Forecasting Services
* Real-Time Demand Prediction
* AI-Powered Inventory Dashboards

---

## Author

**Abhi Patel**

Artificial Intelligence & Machine Learning Student

LaSalle College, Montreal, Canada

---

## License

This repository is intended for educational, research, and portfolio purposes.
