# Data Analytics in the Study of Pavement Deterioration

## Overview
This project analyzes and forecasts pavement deterioration using data analytics and machine learning models. The research was conducted as part of **CEE 4803: Data Analytics in Civil Engineering** and commissioned by the **Florida Department of Transportation (FDOT)**. The study integrates **pavement crack ratings, deterioration rates, and climate data** to optimize maintenance planning and resource allocation.

## Objectives
- Develop a robust forecasting model for pavement conditions over a **5-year period**.
- Identify key factors influencing pavement deterioration.
- Support FDOT’s **budget planning and treatment initiatives**.
- Compare different forecasting models for predictive accuracy and interpretability.

## Data Sources
### **1. FDOT Pavement Dataset**
- Covers **48 years (1976-2023)**.
- Includes attributes such as **crack rating, ride rating, rut rating, cycle age, rehabilitation cycles, ESALs (Equivalent Single Axis Loads), and roadway characteristics**.

### **2. NOAA Climate Data**
- Provides **county-based historical climate data**.
- Includes **temperature, precipitation, drought indices, and seasonal variations**.

## Methodology
### **Data Processing & Feature Engineering**
- Combined FDOT and NOAA datasets, creating a **9304-row by 312-column dataset**.
- Filtered for missing values, outliers, and inconsistencies.
- Engineered new features such as **moving average deterioration rate, climate change impact factors, and roadway characteristics**.

### **Machine Learning Models Used**
| Model | Description | Test MSE |
|--------|------------|-----------|
| **Multiple Linear Regression** | Predicts deterioration rate | **0.0165** |
| **Polynomial Regression** | Fits a polynomial function to crack ratings | **2.867** |
| **ARIMA** | Time series forecasting | **3.005** |
| **Cross-Validated ARIMA** | Optimized ARIMA model | **2.009** |
| **LSTM (Long Short-Term Memory)** | Deep learning model for sequential data | **0.7023** |

- **LSTM outperformed all models**, demonstrating the best accuracy.
- Trade-off: Higher complexity reduces interpretability.

## Key Findings
- **Surface Type and Friction Course** are the most significant predictors of deterioration rate.
- **Climate change factors (temperature, precipitation) have minor statistical significance**.
- **LSTM models significantly outperform traditional statistical models** for long-term pavement condition forecasting.
- **Data inconsistencies and manual crack rating methods introduce noise**, affecting prediction accuracy.

## Future Improvements
- **Incorporate real-time traffic volume data** for better estimations.
- **Enhance climate factor granularity** by integrating sensor-based road data.
- **Further optimize deep learning models (LSTM) using hyperparameter tuning**.
- **Expand analysis to other states** and additional infrastructure assets like **airports and racetracks**.

## Team Members
- **CM**
- **TN**
- **TT**
- **PY**
