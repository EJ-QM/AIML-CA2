# Energy Consumption Forecasting & Customer Analytics

Welcome to the repository for the **Energy Consumption and Customer Analytics** project. This project focuses on analyzing historical utility consumption data (Gas, Electricity, and Water), building robust time-series forecasting models to predict future demand, and exploring customer demographic insights to better understand spending behavior.

---

## ## Project Overview

This project is divided into two primary analytical tracks:

1. **Time-Series Forecasting:** Modeling and predicting 60 periods of future consumption for Gas (tons), Electricity (MWh), and Water (tons) using advanced statistical models like ARIMA, SARIMA, and Exponential Smoothing.
2. **Customer Segmentation & Analytics:** Analyzing customer demographics (Age, Gender, Income) against retail spending habits to uncover key business insights.

---

## ## Dataset Insights & Metadata

The project utilizes two main categories of data:

### ### 1. Energy Consumption Data

Tracks historical utility usage across three main metrics:

* **Date:** Timeline of consumption.
* **Gas Consumption:** Measured in **tons**.
* **Electricity Consumption:** Measured in **MWh**.
* **Water Consumption:** Measured in **tons**.

### ### 2. Customer Data

Demographic and behavioral data collected from utility-associated retail shop profiles:

* **CustomerID:** Unique identifier for each customer.
* **Gender / Age / Income:** Demographics used for segmentation.
* **How Much They Spend:** Customer retail expenditure in dollars ($).

---

## ## Model Performance Metrics

To ensure accurate forecasts, different time-series models were evaluated on test datasets. Below is a summary of how each model performed:

| Model | Mean Absolute Error (MAE) | Root Mean Squared Error (RMSE) | Mean Absolute Percentage Error (MAPE) |
| --- | --- | --- | --- |
| **ARIMA Gas (Test)** | 3.98 | 4.82 | 14.38% |
| **SARIMA Electricity (Test)** | 27.11 | 38.00 | 2.52% |
| **Exponential Smoothing Water (Test)** | 81.31 | 107.06 | 17.90% |

> **Key Takeaway:** The **SARIMA** model performed exceptionally well for Electricity forecasting, achieving a remarkably low error rate (MAPE of **2.52%**), indicating strong seasonal patterns captured by the model.

---

## ## Forecast Summary Statistics

The models generated a **60-period ahead forecast** for all three utilities. The statistical distribution of these forecasts is outlined below:

| Metric | Gas Forecast (tons) | Electricity Forecast (MWh) | Water Forecast (tons) |
| --- | --- | --- | --- |
| **Count** | 60.00 | 60.00 | 60.00 |
| **Mean** | 29.05 | 1,060.19 | 382.10 |
| **Std Dev** | 0.14 | 93.25 | 47.42 |
| **Min** | 29.02 | 922.69 | 300.57 |
| **25%** | 29.02 | 970.02 | 342.81 |
| **50% (Median)** | 29.02 | 1,050.28 | 381.02 |
| **75%** | 29.02 | 1,137.91 | 415.35 |
| **Max** | 30.01 | 1,244.14 | 458.10 |

---

## ## Repository Structure

```text
├── data/
│   ├── energy_consumption.csv          # Historical utility data
│   └── customer_profiles.csv           # Demographic & spending data
├── notebooks/
│   ├── exploratory_data_analysis.ipynb # EDA on customer and energy trends
│   └── time_series_forecasting.ipynb   # Model training and evaluation
├── templates/
│   └── CA2 Meta Data.txt               # Data dictionary and metadata
└── README.md                           # Project documentation

```

---

## ## Getting Started

### ### Prerequisites

Make sure you have the following Python libraries installed:

```bash
pip install pandas numpy statsmodels scikit-learn matplotlib seaborn

```

### ### Running the Analysis

1. Clone this repository to your local machine.
2. Navigate to the `notebooks/` directory.
3. Run `exploratory_data_analysis.ipynb` to view customer spending insights.
4. Run `time_series_forecasting.ipynb` to regenerate the ARIMA, SARIMA, and Exponential Smoothing models.
